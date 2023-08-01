# What maded this playbook

Deploys 3 virtual machines on the cloud: Clickhouse, Lighthouse and Vector. Configures them using configs and installing Nginx and displays the contents of the tables in Lighthouse in a web application.


# Ansible Role: lighthouse

## Description

Deploy [Lighthouse](https://github.com/VKCOM/lighthouse.git) monitoring system using ansible.

## Requirements

- Ansible >= 2.12 

## Role Variables

- `lighthouse_vcs` - repository fot download `lighthouse`;
- `lighthouse_location_dir` - distribution storage location `lighthouse`;
- `lighthouse_access_log_name` - log file name for `nginx`;

#### Example

```
lighthouse_configs:
server {
    listen       80;
    server_name  localhost
    
    access_log  /var/log/nginx {{ lighthouse_access_log_name }}.log  main;
    
    location / {
        root   {{ lighthouse_location_dir }};
        index  index.html;
    }
}
```

## Example

### Playbook

```yaml
- name: Lighthouse | install git
  become: true
  ansible.builtin.yum:
    name: git
    state: present
- name: Lighthouse | Copy from git
  become: true
  ansible.builtin.git:
    repo: "{{ lighthouse_vcs }}"
    version: master
    dest: "{{ lighthouse_location_dir }}"
- name: Lighthouse | Create lighthouse config
  become: true
  ansible.builtin.template:
    src: lighthouse.conf.j2
    dest: /etc/nginx/conf.d/default.conf
    mode: 0644
  notify: Reload nginx
```

# Ansible Role: vector

## Description

Deploy [Vector](https://packages.timber.io/vector) monitoring system using ansible.

## Requirements

- Ansible >= 2.12 

## Role Variables

- `lighthouse_vcs` - repository fot download `lighthouse`;
- `lighthouse_location_dir` - distribution storage location `lighthouse`;
- `lighthouse_access_log_name` - log file name for `nginx`;

#### Example

```
vector_configs:
vector_url: https://packages.timber.io/vector/{{ vector_version }}/vector-{{ vector_version }}-1.x86_64.rpm
vector_version: 0.31.0
nginx_user_name: root
vector_config:
  sources:
      our_log:
        ignore_older_secs: 600
        include:
          - /var/log/nginx/access.log
        read_from: beginning
        type: file
  sinks:
    to_clickhouse:
      type: clickhouse
      inputs:
        - our_log
      database: logs
      endpoint: http://{{ hostvars['clickhouse-01'].ansible_default_ipv4.address }}:8123
      table: access_logs
      compression: gzip
      healthcheck: false
      skip_unknown_fields: true
```

## Example

### Playbook

```yaml
- name: VECTOR | Install rpm
  become: true
  ansible.builtin.yum:
    name: "{{ vector_url }}"
    state: present
- name: VECTOR | Template config
  become: true
  ansible.builtin.template:
    src: templates/vector.yml.j2
    dest: /etc/vector/vector.yml
    mode: '0644'
    owner: "{{ ansible_user_id }}"
    group: "{{ ansible_user_gid }}"
    validate: vector validate --no-environment --config-yaml %s
- name: VECTOR | Create systemd unit
  become: true
  ansible.builtin.template:
    src: templates/vector.service.j2
    dest: /etc/systemd/system/vector.service
    mode: '0644'
    owner: "{{ ansible_user_id }}"
    group: "{{ ansible_user_gid }}"
- name: VECTOR | Start service
  become: true
  ansible.builtin.systemd:
    name: vector
    state: started
    daemon_reload: true
```

# Other important parameters

All repositories addresses are specified in the file: requirements.yml

## Example

```yaml
  - name: clickhouse
    src: git@github.com:AlexeySetevoi/ansible-clickhouse.git
    scm: git
    version: "1.13"
  - name: lighthouse
    src: git@github.com:SemenAmbarnov/lighthouse-role.git
    scm: git
  - name: vector
    src: git@github.com:SemenAmbarnov/vector-role.git
    scm: git
```
## The file inventory/prod.yaml must contain the addresses of virtual machines

## Example

```yaml
---
clickhouse:
  hosts:
    clickhouse-01:
      ansible_host: (ip_vm)
      ansible_ssh_user: (user_name)
lighthouse:
  hosts:
    clickhouse-02:
      ansible_host: (ip_vm)
      ansible_ssh_user: (user_name)
vector:
  hosts:
    clickhouse-03:
      ansible_host: (ip_vm)
      ansible_ssh_user: (user_name)

