# DEPRECATED

# Ansible Role: lighthouse

## Description

Deploy [Lighthouse](https://github.com/VKCOM/lighthouse.git) monitoring system using ansible.

## Requirements

- Ansible >= 2.12 

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `prometheus_version` | 2.27.0 | Prometheus package version. Also accepts `latest` as parameter. Only prometheus 2.x is supported |
| `prometheus_skip_install` | false | Prometheus installation tasks gets skipped when set to true. |
| `prometheus_binary_local_dir` | "" | Allows to use local packages instead of ones distributed on github. As parameter it takes a directory where `prometheus` AND `promtool` binaries are stored on host on which ansible is ran. This overrides `prometheus_version` parameter |
| `prometheus_config_dir` | /etc/prometheus | Path to directory with prometheus configuration |
| `prometheus_db_dir` | /var/lib/prometheus | Path to directory with prometheus database |
| `prometheus_read_only_dirs`| [] | Additional paths that Prometheus is allowed to read (useful for SSL certs outside of the config directory) |
| `prometheus_web_listen_address` | "0.0.0.0:9090" | Address on which prometheus will be listening |
| `prometheus_web_config` | {} | A Prometheus [web config yaml](https://github.com/prometheus/exporter-toolkit/blob/master/docs/web-configuration.md) for configuring TLS and auth. |
| `prometheus_web_external_url` | "" | External address on which prometheus is available. Useful when behind reverse proxy. Ex. `http://example.org/prometheus` |
| `prometheus_storage_retention` | "30d" | Data retention period |
| `prometheus_storage_retention_size` | "0" | Data retention period by size |
| `prometheus_config_flags_extra` | {} | Additional configuration flags passed to prometheus binary at startup |
| `prometheus_alertmanager_config` | [] | Configuration responsible for pointing where alertmanagers are. This should be specified as list in yaml format. It is compatible with official [<alertmanager_config>](https://prometheus.io/docs/prometheus/latest/configuration/configuration/#alertmanager_config) |
| `prometheus_alert_relabel_configs` | [] | Alert relabeling rules. This should be specified as list in yaml format. It is compatible with the official [<alert_relabel_configs>](https://prometheus.io/docs/prometheus/latest/configuration/configuration/#alert_relabel_configs) |
| `prometheus_global` | { scrape_interval: 60s, scrape_timeout: 15s, evaluation_interval: 15s } | Prometheus global config. Compatible with [official configuration](https://prometheus.io/docs/prometheus/latest/configuration/configuration/#configuration-file) |
| `prometheus_remote_write` | [] | Remote write. Compatible with [official configuration](https://prometheus.io/docs/prometheus/latest/configuration/configuration/#<remote_write>) |
| `prometheus_remote_read` | [] | Remote read. Compatible with [official configuration](https://prometheus.io/docs/prometheus/latest/configuration/configuration/#<remote_read>) |
| `prometheus_external_labels` | environment: "{{ ansible_fqdn \| default(ansible_host) \| default(inventory_hostname) }}" | Provide map of additional labels which will be added to any time series or alerts when communicating with external systems |
| `prometheus_targets` | {} | Targets which will be scraped. Better example is provided in our [demo site](https://github.com/cloudalchemy/demo-site/blob/2a8a56fc10ce613d8b08dc8623230dace6704f9a/group_vars/all/vars#L8) |
| `prometheus_scrape_configs` | [defaults/main.yml#L58](https://github.com/cloudalchemy/ansible-prometheus/blob/ff7830d06ba57be1177f2b6fca33a4dd2d97dc20/defaults/main.yml#L47) | Prometheus scrape jobs provided in same format as in [official docs](https://prometheus.io/docs/prometheus/latest/configuration/configuration/#scrape_config) |
| `prometheus_config_file` | "prometheus.yml.j2" | Variable used to provide custom prometheus configuration file in form of ansible template |
| `prometheus_alert_rules` | [defaults/main.yml#L81](https://github.com/cloudalchemy/ansible-prometheus/blob/73d6df05a775ee5b736ac8f28d5605f2a975d50a/defaults/main.yml#L85) | Full list of alerting rules which will be copied to `{{ prometheus_config_dir }}/rules/ansible_managed.rules`. Alerting rules can be also provided by other files located in `{{ prometheus_config_dir }}/rules/` which have `*.rules` extension |
| `prometheus_alert_rules_files` | [defaults/main.yml#L78](https://github.com/cloudalchemy/ansible-prometheus/blob/73d6df05a775ee5b736ac8f28d5605f2a975d50a/defaults/main.yml#L78) | List of folders where ansible will look for files containing alerting rules which will be copied to `{{ prometheus_config_dir }}/rules/`. Files must have `*.rules` extension |
| `prometheus_static_targets_files` | [defaults/main.yml#L78](https://github.com/cloudalchemy/ansible-prometheus/blob/73d6df05a775ee5b736ac8f28d5605f2a975d50a/defaults/main.yml#L81) | List of folders where ansible will look for files containing custom static target configuration files which will be copied to `{{ prometheus_config_dir }}/file_sd/`. |


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
