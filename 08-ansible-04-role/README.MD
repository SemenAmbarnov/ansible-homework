# Whatt maded this playbook

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
