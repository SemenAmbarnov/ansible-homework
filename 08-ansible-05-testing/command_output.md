## Основная часть

Ваша цель — настроить тестирование ваших ролей. 

Задача — сделать сценарии тестирования для vector. 

Ожидаемый результат — все сценарии успешно проходят тестирование ролей.

### Molecule

1. Запустите  `molecule test -s centos_7` внутри корневой директории clickhouse-role, посмотрите на вывод команды. Данная команда может отработать с ошибками, это нормально. Наша цель - посмотреть как другие в реальном мире используют молекулу.
```
[sam@localhost clickhouse]$ molecule test -s centos_7
INFO     centos_7 scenario test matrix: dependency, lint, cleanup, destroy, syntax, create, prepare, converge, idempotence, side_effect, verify, cleanup, destroy
INFO     Performing prerun...
INFO     Set ANSIBLE_LIBRARY=/home/sam/.cache/ansible-compat/6182d2/modules:/home/sam/.ansible/plugins/modules:/usr/share/ansible/plugins/modules
INFO     Set ANSIBLE_COLLECTIONS_PATH=/home/sam/.cache/ansible-compat/6182d2/collections:/home/sam/.ansible/collections:/usr/share/ansible/collections
INFO     Set ANSIBLE_ROLES_PATH=/home/sam/.cache/ansible-compat/6182d2/roles:/home/sam/.ansible/roles:/usr/share/ansible/roles:/etc/ansible/roles
INFO     Inventory /home/sam/homework/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/hosts.yml linked to /home/sam/.cache/molecule/clickhouse/centos_7/inventory/hosts
INFO     Inventory /home/sam/homework/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/group_vars/ linked to /home/sam/.cache/molecule/clickhouse/centos_7/inventory/group_vars
INFO     Inventory /home/sam/homework/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/host_vars/ linked to /home/sam/.cache/molecule/clickhouse/centos_7/inventory/host_vars
INFO     Running centos_7 > dependency
WARNING  Skipping, missing the requirements file.
WARNING  Skipping, missing the requirements file.
INFO     Inventory /home/sam/homework/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/hosts.yml linked to /home/sam/.cache/molecule/clickhouse/centos_7/inventory/hosts
INFO     Inventory /home/sam/homework/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/group_vars/ linked to /home/sam/.cache/molecule/clickhouse/centos_7/inventory/group_vars
INFO     Inventory /home/sam/homework/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/host_vars/ linked to /home/sam/.cache/molecule/clickhouse/centos_7/inventory/host_vars
INFO     Running centos_7 > lint
COMMAND: yamllint .
ansible-lint
flake8
/bin/bash: line 2: flake8: command not found
CRITICAL Lint failed with error code 127
WARNING  An error occurred during the test sequence action: 'lint'. Cleaning up.
INFO     Inventory /home/sam/homework/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/hosts.yml linked to /home/sam/.cache/molecule/clickhouse/centos_7/inventory/hosts
INFO     Inventory /home/sam/homework/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/group_vars/ linked to /home/sam/.cache/molecule/clickhouse/centos_7/inventory/group_vars
INFO     Inventory /home/sam/homework/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/host_vars/ linked to /home/sam/.cache/molecule/clickhouse/centos_7/inventory/host_vars
INFO     Running centos_7 > cleanup
WARNING  Skipping, cleanup playbook not configured.
INFO     Inventory /home/sam/homework/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/hosts.yml linked to /home/sam/.cache/molecule/clickhouse/centos_7/inventory/hosts
INFO     Inventory /home/sam/homework/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/group_vars/ linked to /home/sam/.cache/molecule/clickhouse/centos_7/inventory/group_vars
INFO     Inventory /home/sam/homework/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/host_vars/ linked to /home/sam/.cache/molecule/clickhouse/centos_7/inventory/host_vars
INFO     Running centos_7 > destroy
INFO     Sanity checks: 'docker'

PLAY [Destroy] *****************************************************************

TASK [Destroy molecule instance(s)] ********************************************
changed: [localhost] => (item=centos_7)

TASK [Wait for instance(s) deletion to complete] *******************************
ok: [localhost] => (item=centos_7)

TASK [Delete docker networks(s)] ***********************************************
skipping: [localhost]

PLAY RECAP *********************************************************************
localhost                  : ok=2    changed=1    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

INFO     Pruning extra files from scenario ephemeral directory
```


2. Перейдите в каталог с ролью vector-role и создайте сценарий тестирования по умолчанию при помощи `molecule init scenario --driver-name docker`.

Сделано

3. Добавьте несколько разных дистрибутивов (centos:8, ubuntu:latest) для инстансов и протестируйте роль, исправьте найденные ошибки, если они есть.

```
[sam@localhost vector]$ molecule test -s centos_7
INFO     centos_7 scenario test matrix: dependency, lint, cleanup, destroy, syntax, create, prepare, converge, idempotence, side_effect, verify, cleanup, destroy
INFO     Performing prerun...
INFO     Set ANSIBLE_LIBRARY=/home/sam/.cache/ansible-compat/c5717f/modules:/home/sam/.ansible/plugins/modules:/usr/share/ansible/plugins/modules
INFO     Set ANSIBLE_COLLECTIONS_PATH=/home/sam/.cache/ansible-compat/c5717f/collections:/home/sam/.ansible/collections:/usr/share/ansible/collections
INFO     Set ANSIBLE_ROLES_PATH=/home/sam/.cache/ansible-compat/c5717f/roles:/home/sam/.ansible/roles:/usr/share/ansible/roles:/etc/ansible/roles
INFO     Running centos_7 > dependency
WARNING  Skipping, missing the requirements file.
WARNING  Skipping, missing the requirements file.
INFO     Running centos_7 > lint
INFO     Lint is disabled.
INFO     Running centos_7 > cleanup
WARNING  Skipping, cleanup playbook not configured.
INFO     Running centos_7 > destroy
INFO     Sanity checks: 'docker'

PLAY [Destroy] *****************************************************************

TASK [Destroy molecule instance(s)] ********************************************
changed: [localhost] => (item=instance)

TASK [Wait for instance(s) deletion to complete] *******************************
ok: [localhost] => (item=instance)

TASK [Delete docker networks(s)] ***********************************************
skipping: [localhost]

PLAY RECAP *********************************************************************
localhost                  : ok=2    changed=1    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

INFO     Running centos_7 > syntax

playbook: /home/sam/homework/playbook/roles/vector/molecule/centos_7/converge.yml
INFO     Running centos_7 > create

PLAY [Create] ******************************************************************

TASK [Log into a Docker registry] **********************************************
skipping: [localhost] => (item=None) 
skipping: [localhost]

TASK [Check presence of custom Dockerfiles] ************************************
ok: [localhost] => (item={'image': 'quay.io/centos/centos:7', 'name': 'instance', 'pre_build_image': True})

TASK [Create Dockerfiles from image names] *************************************
skipping: [localhost] => (item={'image': 'quay.io/centos/centos:7', 'name': 'instance', 'pre_build_image': True}) 
skipping: [localhost]

TASK [Discover local Docker images] ********************************************
ok: [localhost] => (item={'changed': False, 'skipped': True, 'skip_reason': 'Conditional result was False', 'false_condition': 'not item.pre_build_image | default(false)', 'item': {'image': 'quay.io/centos/centos:7', 'name': 'instance', 'pre_build_image': True}, 'ansible_loop_var': 'item', 'i': 0, 'ansible_index_var': 'i'})

TASK [Build an Ansible compatible image (new)] *********************************
skipping: [localhost] => (item=molecule_local/quay.io/centos/centos:7) 
skipping: [localhost]

TASK [Create docker network(s)] ************************************************
skipping: [localhost]

TASK [Determine the CMD directives] ********************************************
ok: [localhost] => (item={'image': 'quay.io/centos/centos:7', 'name': 'instance', 'pre_build_image': True})

TASK [Create molecule instance(s)] *********************************************
changed: [localhost] => (item=instance)

TASK [Wait for instance(s) creation to complete] *******************************
FAILED - RETRYING: [localhost]: Wait for instance(s) creation to complete (300 retries left).
changed: [localhost] => (item={'failed': 0, 'started': 1, 'finished': 0, 'ansible_job_id': 'j887707150370.63612', 'results_file': '/home/sam/.ansible_async/j887707150370.63612', 'changed': True, 'item': {'image': 'quay.io/centos/centos:7', 'name': 'instance', 'pre_build_image': True}, 'ansible_loop_var': 'item'})

PLAY RECAP *********************************************************************
localhost                  : ok=5    changed=2    unreachable=0    failed=0    skipped=4    rescued=0    ignored=0

INFO     Running centos_7 > prepare
WARNING  Skipping, prepare playbook not configured.
INFO     Running centos_7 > converge

PLAY [Converge] ****************************************************************

TASK [Gathering Facts] *********************************************************
ok: [instance]

TASK [Install sudo] ************************************************************
changed: [instance]

TASK [Include vector-role] *****************************************************

TASK [vector : Install vector] *************************************************
included: /home/sam/homework/playbook/roles/vector/tasks/install_vector_docker.yml for instance

TASK [vector : VECTOR | Install rpm] *******************************************
changed: [instance]

TASK [vector : VECTOR | Template config] ***************************************
changed: [instance]

TASK [vector : Install vector] *************************************************
skipping: [instance]

PLAY RECAP *********************************************************************
instance                   : ok=5    changed=3    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

INFO     Running centos_7 > idempotence

PLAY [Converge] ****************************************************************

TASK [Gathering Facts] *********************************************************
ok: [instance]

TASK [Install sudo] ************************************************************
ok: [instance]

TASK [Include vector-role] *****************************************************

TASK [vector : Install vector] *************************************************
included: /home/sam/homework/playbook/roles/vector/tasks/install_vector_docker.yml for instance

TASK [vector : VECTOR | Install rpm] *******************************************
ok: [instance]

TASK [vector : VECTOR | Template config] ***************************************
ok: [instance]

TASK [vector : Install vector] *************************************************
skipping: [instance]

PLAY RECAP *********************************************************************
instance                   : ok=5    changed=0    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

INFO     Idempotence completed successfully.
INFO     Running centos_7 > side_effect
WARNING  Skipping, side effect playbook not configured.
INFO     Running centos_7 > verify
INFO     Running Ansible Verifier

PLAY [Verify] ******************************************************************

TASK [Example assertion] *******************************************************
ok: [instance] => {
    "changed": false,
    "msg": "All assertions passed"
}

TASK [Check NGINX configs] *****************************************************
changed: [instance]

TASK [Check NGINX status] ******************************************************
changed: [instance]

PLAY RECAP *********************************************************************
instance                   : ok=3    changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

INFO     Verifier completed successfully.
INFO     Running centos_7 > cleanup
WARNING  Skipping, cleanup playbook not configured.
INFO     Running centos_7 > destroy

PLAY [Destroy] *****************************************************************

TASK [Destroy molecule instance(s)] ********************************************
changed: [localhost] => (item=instance)

TASK [Wait for instance(s) deletion to complete] *******************************
FAILED - RETRYING: [localhost]: Wait for instance(s) deletion to complete (300 retries left).
changed: [localhost] => (item=instance)

TASK [Delete docker networks(s)] ***********************************************
skipping: [localhost]

PLAY RECAP *********************************************************************
localhost                  : ok=2    changed=2    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

INFO     Pruning extra files from scenario ephemeral directory
```

4. Добавьте несколько assert в verify.yml-файл для  проверки работоспособности vector-role (проверка, что конфиг валидный, проверка успешности запуска и др.). 

```
---
# This is an example playbook to execute Ansible tests.

- name: Verify
  hosts: all
  gather_facts: false
  tasks:
  - name: Example assertion
    assert:
      that: true
  - name: Check NGINX configs
    shell: vector validate --no-environment --config-yaml /etc/vector/vector.yml
  - name: Check NGINX status
    shell: ps aux | grep vector
```
5. Запустите тестирование роли повторно и проверьте, что оно прошло успешно.

```
PLAY [Verify] ******************************************************************

TASK [Example assertion] *******************************************************
ok: [instance] => {
    "changed": false,
    "msg": "All assertions passed"
}

TASK [Check NGINX configs] *****************************************************
changed: [instance]

TASK [Check NGINX status] ******************************************************
changed: [instance]

PLAY RECAP *********************************************************************
instance                   : ok=3    changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

INFO     Verifier completed successfully.
INFO     Running centos_7 > cleanup
```
   
6. Добавьте новый тег на коммит с рабочим сценарием в соответствии с семантическим версионированием.

### Tox

1. Добавьте в директорию с vector-role файлы из [директории](./example).
2. Запустите `docker run --privileged=True -v <path_to_repo>:/opt/vector-role -w /opt/vector-role -it aragast/netology:latest /bin/bash`, где path_to_repo — путь до корня репозитория с vector-role на вашей файловой системе.
3. Внутри контейнера выполните команду `tox`, посмотрите на вывод.
5. Создайте облегчённый сценарий для `molecule` с драйвером `molecule_podman`. Проверьте его на исполнимость.
6. Пропишите правильную команду в `tox.ini`, чтобы запускался облегчённый сценарий.
8. Запустите команду `tox`. Убедитесь, что всё отработало успешно.
9. Добавьте новый тег на коммит с рабочим сценарием в соответствии с семантическим версионированием.

После выполнения у вас должно получится два сценария molecule и один tox.ini файл в репозитории. Не забудьте указать в ответе теги решений Tox и Molecule заданий. В качестве решения пришлите ссылку на  ваш репозиторий и скриншоты этапов выполнения задания
