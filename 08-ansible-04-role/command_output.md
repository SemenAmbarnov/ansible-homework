# Так как данный плейбук по назначению и работе идентичен плейбуку из предыдущего урока то здесь выкладываю вывод из терминала. И скрин вебморды Vector после окончания работы плейбука.


```
[sam@localhost playbook]$ ansible-galaxy install -r requirements.yml -p roles
Starting galaxy role install process
[sam@localhost playbook]$ ansible-playbook -i inventory/prod.yml site.yml

PLAY [Install Clickhouse] ***************************************************************************************************************************************************************************

TASK [Gathering Facts] ******************************************************************************************************************************************************************************
The authenticity of host '158.160.102.126 (158.160.102.126)' can't be established.
ECDSA key fingerprint is SHA256:VMWZi8ulCseF+pZuDBxCdCSduM2A2DyfDSJyuIhF9no.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
ok: [clickhouse-01]

TASK [clickhouse : Include OS Family Specific Variables] ********************************************************************************************************************************************
ok: [clickhouse-01]

TASK [clickhouse : include_tasks] *******************************************************************************************************************************************************************
included: /home/sam/homework/playbook/roles/clickhouse/tasks/precheck.yml for clickhouse-01

TASK [clickhouse : Requirements check | Checking sse4_2 support] ************************************************************************************************************************************
ok: [clickhouse-01]

TASK [clickhouse : Requirements check | Not supported distribution && release] **********************************************************************************************************************
skipping: [clickhouse-01]

TASK [clickhouse : include_tasks] *******************************************************************************************************************************************************************
included: /home/sam/homework/playbook/roles/clickhouse/tasks/params.yml for clickhouse-01

TASK [clickhouse : Set clickhouse_service_enable] ***************************************************************************************************************************************************
ok: [clickhouse-01]

TASK [clickhouse : Set clickhouse_service_ensure] ***************************************************************************************************************************************************
ok: [clickhouse-01]

TASK [clickhouse : include_tasks] *******************************************************************************************************************************************************************
included: /home/sam/homework/playbook/roles/clickhouse/tasks/install/yum.yml for clickhouse-01

TASK [clickhouse : Install by YUM | Ensure clickhouse repo installed] *******************************************************************************************************************************
changed: [clickhouse-01]

TASK [clickhouse : Install by YUM | Ensure clickhouse package installed (latest)] *******************************************************************************************************************
changed: [clickhouse-01]

TASK [clickhouse : Install by YUM | Ensure clickhouse package installed (version latest)] ***********************************************************************************************************
skipping: [clickhouse-01]

TASK [clickhouse : include_tasks] *******************************************************************************************************************************************************************
included: /home/sam/homework/playbook/roles/clickhouse/tasks/configure/sys.yml for clickhouse-01

TASK [clickhouse : Check clickhouse config, data and logs] ******************************************************************************************************************************************
ok: [clickhouse-01] => (item=/var/log/clickhouse-server)
changed: [clickhouse-01] => (item=/etc/clickhouse-server)
changed: [clickhouse-01] => (item=/var/lib/clickhouse/tmp/)
changed: [clickhouse-01] => (item=/var/lib/clickhouse/)

TASK [clickhouse : Config | Create config.d folder] *************************************************************************************************************************************************
changed: [clickhouse-01]

TASK [clickhouse : Config | Create users.d folder] **************************************************************************************************************************************************
changed: [clickhouse-01]

TASK [clickhouse : Config | Generate system config] *************************************************************************************************************************************************
changed: [clickhouse-01]

TASK [clickhouse : Config | Generate users config] **************************************************************************************************************************************************
changed: [clickhouse-01]

TASK [clickhouse : Config | Generate remote_servers config] *****************************************************************************************************************************************
skipping: [clickhouse-01]

TASK [clickhouse : Config | Generate macros config] *************************************************************************************************************************************************
skipping: [clickhouse-01]

TASK [clickhouse : Config | Generate zookeeper servers config] **************************************************************************************************************************************
skipping: [clickhouse-01]

TASK [clickhouse : Config | Fix interserver_http_port and intersever_https_port collision] **********************************************************************************************************
skipping: [clickhouse-01]

TASK [clickhouse : Notify Handlers Now] *************************************************************************************************************************************************************

RUNNING HANDLER [clickhouse : Restart Clickhouse Service] *******************************************************************************************************************************************
ok: [clickhouse-01]

TASK [clickhouse : include_tasks] *******************************************************************************************************************************************************************
included: /home/sam/homework/playbook/roles/clickhouse/tasks/service.yml for clickhouse-01

TASK [clickhouse : Ensure clickhouse-server.service is enabled: True and state: restarted] **********************************************************************************************************
changed: [clickhouse-01]

TASK [clickhouse : Wait for Clickhouse Server to Become Ready] **************************************************************************************************************************************
ok: [clickhouse-01]

TASK [clickhouse : include_tasks] *******************************************************************************************************************************************************************
included: /home/sam/homework/playbook/roles/clickhouse/tasks/configure/db.yml for clickhouse-01

TASK [clickhouse : Set ClickHose Connection String] *************************************************************************************************************************************************
ok: [clickhouse-01]

TASK [clickhouse : Gather list of existing databases] ***********************************************************************************************************************************************
ok: [clickhouse-01]

TASK [clickhouse : Config | Delete database config] *************************************************************************************************************************************************
skipping: [clickhouse-01]

TASK [clickhouse : Config | Create database config] *************************************************************************************************************************************************
skipping: [clickhouse-01]

TASK [clickhouse : include_tasks] *******************************************************************************************************************************************************************
included: /home/sam/homework/playbook/roles/clickhouse/tasks/configure/dict.yml for clickhouse-01

TASK [clickhouse : Config | Generate dictionary config] *********************************************************************************************************************************************
skipping: [clickhouse-01]

TASK [clickhouse : include_tasks] *******************************************************************************************************************************************************************
skipping: [clickhouse-01]

PLAY [Install Lighthouse] ***************************************************************************************************************************************************************************

TASK [Gathering Facts] ******************************************************************************************************************************************************************************
The authenticity of host '158.160.39.170 (158.160.39.170)' can't be established.
ECDSA key fingerprint is SHA256:LA97b0+eqRa6SlHFMoKR4plk6vKMaXTHKf4YnP903sg.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
ok: [clickhouse-02]

TASK [lighthouse : include_tasks] *******************************************************************************************************************************************************************
included: /home/sam/homework/playbook/roles/lighthouse/tasks/install_lighthouse.yml for clickhouse-02

TASK [lighthouse : NGINX | Install eper-release] ****************************************************************************************************************************************************
changed: [clickhouse-02]

TASK [lighthouse : NGINX | Install Nginx] ***********************************************************************************************************************************************************
changed: [clickhouse-02]

TASK [lighthouse : NGINX | Create general config] ***************************************************************************************************************************************************
changed: [clickhouse-02]

TASK [lighthouse : Lighthouse | install git] ********************************************************************************************************************************************************
changed: [clickhouse-02]

TASK [lighthouse : Lighthouse | Copy from git] ******************************************************************************************************************************************************
changed: [clickhouse-02]

TASK [lighthouse : Lighthouse | Create lighthouse config] *******************************************************************************************************************************************
changed: [clickhouse-02]

RUNNING HANDLER [lighthouse : Start nginx] **********************************************************************************************************************************************************
changed: [clickhouse-02]

RUNNING HANDLER [lighthouse : Reload nginx] *********************************************************************************************************************************************************
changed: [clickhouse-02]

PLAY [Install Vector] *******************************************************************************************************************************************************************************

TASK [Gathering Facts] ******************************************************************************************************************************************************************************
The authenticity of host '158.160.63.238 (158.160.63.238)' can't be established.
ECDSA key fingerprint is SHA256:ViNxv/N5NKMCi9o4vVk8YBbI5N4/0ALw+8X5T/0mj3U.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
ok: [clickhouse-03]

TASK [vector : NGINX | Install eper-release] ********************************************************************************************************************************************************
changed: [clickhouse-03]

TASK [vector : NGINX | Install Nginx] ***************************************************************************************************************************************************************
changed: [clickhouse-03]

TASK [vector : NGINX | Create general config] *******************************************************************************************************************************************************
changed: [clickhouse-03]

TASK [vector : VECTOR | Install rpm] ****************************************************************************************************************************************************************
changed: [clickhouse-03]

TASK [vector : VECTOR | Template config] ************************************************************************************************************************************************************
changed: [clickhouse-03]

TASK [vector : VECTOR | Create systemd unit] ********************************************************************************************************************************************************
changed: [clickhouse-03]

TASK [vector : VECTOR | Start service] **************************************************************************************************************************************************************
changed: [clickhouse-03]

RUNNING HANDLER [vector : Start nginx] **************************************************************************************************************************************************************
changed: [clickhouse-03]

RUNNING HANDLER [vector : Reload nginx] *************************************************************************************************************************************************************
changed: [clickhouse-03]

PLAY RECAP ******************************************************************************************************************************************************************************************
clickhouse-01              : ok=24   changed=8    unreachable=0    failed=0    skipped=10   rescued=0    ignored=0   
clickhouse-02              : ok=10   changed=8    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
clickhouse-03              : ok=10   changed=9    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
```
![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/8f651dba-a21a-45cb-a427-a97414fd3bb3)
