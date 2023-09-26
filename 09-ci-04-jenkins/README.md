## Основная часть

1. Сделать Freestyle Job, который будет запускать `molecule test` из любого вашего репозитория с ролью.

![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/b2efa7ff-b136-4494-a2f0-6c7d3bf363c3) \

```
21:16:01 Started by user admin
21:16:01 Running as SYSTEM
21:16:01 Building remotely on node1 (linux) in workspace /opt/jenkins_agent/workspace/vector-role
21:16:01 [WS-CLEANUP] Deleting project workspace...
21:16:01 [WS-CLEANUP] Deferred wipeout is disabled by the node property...
21:16:01 The recommended git tool is: NONE
21:16:01 using credential f4832340-5da4-45a7-abd6-e57396fa3262
21:16:01 Cloning the remote Git repository
21:16:01 Cloning repository git@github.com:SemenAmbarnov/vector-role.git
21:16:01  > git init /opt/jenkins_agent/workspace/vector-role # timeout=10
21:16:01 Fetching upstream changes from git@github.com:SemenAmbarnov/vector-role.gi
21:16:01  > git --version # timeout=10
21:16:01  > git --version # 'git version 1.8.3.1'
21:16:01 using GIT_SSH to set credentials 
21:16:01 [INFO] Currently running in a labeled security context
21:16:01 [INFO] Currently SELinux is 'enforcing' on the host
21:16:01  > /usr/bin/chcon --type=ssh_home_t /opt/jenkins_agent/workspace/vector-role@tmp/jenkins-gitclient-ssh17540435216824274410.key
21:16:01  > git fetch --tags --progress git@github.com:SemenAmbarnov/vector-role.gi +refs/heads/*:refs/remotes/origin/* # timeout=10
21:16:02  > git config remote.origin.url git@github.com:SemenAmbarnov/vector-role.gi # timeout=10
21:16:02  > git config --add remote.origin.fetch +refs/heads/*:refs/remotes/origin/* # timeout=10
21:16:02 Avoid second fetch
21:16:02  > git rev-parse refs/remotes/origin/main^{commit} # timeout=10
21:16:02 Checking out Revision fac31dc5a70650c81c7f55aad1e97bd523676dbc (refs/remotes/origin/main)
21:16:02  > git config core.sparsecheckout # timeout=10
21:16:02  > git checkout -f fac31dc5a70650c81c7f55aad1e97bd523676dbc # timeout=10
21:16:02 Commit message: "v1.2.1"
21:16:02  > git rev-list --no-walk fac31dc5a70650c81c7f55aad1e97bd523676dbc # timeout=10
21:16:02 [roles-vector] $ /bin/sh -xe /tmp/jenkins9923216029577647147.sh
21:16:02 + molecule --version
21:16:03 molecule 3.4.0 using python 3.6 
21:16:03     ansible:2.10.17
21:16:03     delegated:3.4.0 from molecule
21:16:03     docker:1.1.0 from molecule_docker requiring collections: community.docker>=1.9.1
21:16:03 + molecule test -s centos7
21:16:04 INFO     centos7 scenario test matrix: dependency, lint, cleanup, destroy, syntax, create, prepare, converge, idempotence, side_effect, verify, cleanup, destroy
21:16:04 INFO     Performing prerun...
21:16:04 INFO     Guessed /opt/jenkins_agent/workspace/roles-vector as project root directory
21:16:04 WARNING  Computed fully qualified role name of panmonster.roles-vector does not follow current galaxy requirements.
21:16:04 Please edit meta/main.yml and assure we can correctly determine full role name:
21:16:04 
21:16:04 galaxy_info:
21:16:04 role_name: my_name  # if absent directory name hosting role is used instead
21:16:04 namespace: my_galaxy_namespace  # if absent, author is used instead
21:16:04 
21:16:04 Namespace: https://galaxy.ansible.com/docs/contributing/namespaces.html#galaxy-namespace-limitations
21:16:04 Role: https://galaxy.ansible.com/docs/contributing/creating_role.html#role-names
21:16:04 
21:16:04 As an alternative, you can add 'role-name' to either skip_list or warn_list.
21:16:04 
21:16:04 INFO     Using /home/jenkins/.cache/ansible-lint/04b2fc/roles/panmonster.roles-vector symlink to current repository in order to enable Ansible to find the role using its expected full name.
21:16:04 INFO     Added ANSIBLE_ROLES_PATH=~/.ansible/roles:/usr/share/ansible/roles:/etc/ansible/roles:/home/jenkins/.cache/ansible-lint/04b2fc/roles
21:16:04 INFO     Running centos7 > dependency
21:16:05 /usr/local/lib/python3.6/site-packages/ansible/parsing/vault/__init__.py:44: CryptographyDeprecationWarning: Python 3.6 is no longer supported by the Python core team. Therefore, support for it is deprecated in cryptography and will be removed in a future release.
21:16:05   from cryptography.exceptions import InvalidSignature
21:16:05 WARNING  Skipping, missing the requirements file.
21:16:05 /usr/local/lib/python3.6/site-packages/ansible/parsing/vault/__init__.py:44: CryptographyDeprecationWarning: Python 3.6 is no longer supported by the Python core team. Therefore, support for it is deprecated in cryptography and will be removed in a future release.
21:16:05   from cryptography.exceptions import InvalidSignature
21:16:05 WARNING  Skipping, missing the requirements file.
21:16:05 INFO     Running centos7 > lint
21:16:05 INFO     Lint is disabled.
21:16:05 INFO     Running centos7 > cleanup
21:16:05 WARNING  Skipping, cleanup playbook not configured.
21:16:05 INFO     Running centos7 > destroy
21:16:05 INFO     Sanity checks: 'docker'
21:16:05 /home/jenkins/.local/lib/python3.6/site-packages/paramiko/transport.py:33: CryptographyDeprecationWarning: Python 3.6 is no longer supported by the Python core team. Therefore, support for it is deprecated in cryptography and will be removed in a future release.
21:16:05   from cryptography.hazmat.backends import default_backend
21:16:06 
21:16:06 PLAY [Destroy] *****************************************************************
21:16:06 
21:16:06 TASK [Destroy molecule instance(s)] ********************************************
21:16:06 /usr/local/lib/python3.6/site-packages/ansible/parsing/vault/__init__.py:44: CryptographyDeprecationWarning: Python 3.6 is no longer supported by the Python core team. Therefore, support for it is deprecated in cryptography and will be removed in a future release.
21:16:06   from cryptography.exceptions import InvalidSignature
21:16:06 changed: [localhost] => (item=instance)
21:16:06 
21:16:06 TASK [Wait for instance(s) deletion to complete] *******************************
21:16:07 FAILED - RETRYING: Wait for instance(s) deletion to complete (300 retries left).
21:16:12 ok: [localhost] => (item=instance)
21:16:12 
21:16:12 TASK [Delete docker networks(s)] ***********************************************
21:16:12 
21:16:12 PLAY RECAP *********************************************************************
21:16:12 localhost                  : ok=2    changed=1    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0
21:16:12 
21:16:12 INFO     Running centos7 > syntax
21:16:12 
21:16:12 playbook: /opt/jenkins_agent/workspace/vector-role/molecule/centos7/converge.yml
21:16:12 /usr/local/lib/python3.6/site-packages/ansible/parsing/vault/__init__.py:44: CryptographyDeprecationWarning: Python 3.6 is no longer supported by the Python core team. Therefore, support for it is deprecated in cryptography and will be removed in a future release.
21:16:12   from cryptography.exceptions import InvalidSignature
21:16:12 INFO     Running centos7 > create
21:16:13 
21:16:13 PLAY [Create] ******************************************************************
21:16:13 
21:16:13 TASK [Log into a Docker registry] **********************************************
21:16:13 /usr/local/lib/python3.6/site-packages/ansible/parsing/vault/__init__.py:44: CryptographyDeprecationWarning: Python 3.6 is no longer supported by the Python core team. Therefore, support for it is deprecated in cryptography and will be removed in a future release.
21:16:13   from cryptography.exceptions import InvalidSignature
21:16:13 skipping: [localhost] => (item=None)
21:16:13 skipping: [localhost]
21:16:13 
21:16:13 TASK [Check presence of custom Dockerfiles] ************************************
21:16:13 ok: [localhost] => (item={'image': 'centos7', 'name': 'instance', 'pre_build_image': True})
21:16:13 
21:16:13 TASK [Create Dockerfiles from image names] *************************************
21:16:13 skipping: [localhost] => (item={'image': 'centos7', 'name': 'instance', 'pre_build_image': True})
21:16:13 
21:16:13 TASK [Discover local Docker images] ********************************************
21:16:14 ok: [localhost] => (item={'changed': False, 'skipped': True, 'skip_reason': 'Conditional result was False', 'item': {'image': 'centos7', 'name': 'instance', 'pre_build_image': True}, 'ansible_loop_var': 'item', 'i': 0, 'ansible_index_var': 'i'})
21:16:14 
21:16:14 TASK [Build an Ansible compatible image (new)] *********************************
21:16:14 skipping: [localhost] => (item=molecule_local/centos7)
21:16:14 
21:16:14 TASK [Create docker network(s)] ************************************************
21:16:14 
21:16:14 TASK [Determine the CMD directives] ********************************************
21:16:14 ok: [localhost] => (item={'image': 'centos7', 'name': 'instance', 'pre_build_image': True})
21:16:14 
21:16:14 TASK [Create molecule instance(s)] *********************************************
21:16:15 changed: [localhost] => (item=instance)
21:16:15 
21:16:15 TASK [Wait for instance(s) creation to complete] *******************************
21:16:15 FAILED - RETRYING: Wait for instance(s) creation to complete (300 retries left).
21:16:20 changed: [localhost] => (item={'started': 1, 'finished': 0, 'ansible_job_id': '25425352215.916', 'results_file': '/home/jenkins/.ansible_async/25425352215.916', 'changed': True, 'failed': False, 'item': {'image': 'centos7', 'name': 'instance', 'pre_build_image': True}, 'ansible_loop_var': 'item'})
21:16:20 
21:16:20 PLAY RECAP *********************************************************************
21:16:20 localhost                  : ok=5    changed=2    unreachable=0    failed=0    skipped=4    rescued=0    ignored=0
21:16:20 
21:16:20 INFO     Running centos7 > prepare
21:16:20 WARNING  Skipping, prepare playbook not configured.
21:16:20 INFO     Running centos7 > converge
21:16:21 
21:16:21 PLAY [Converge] ****************************************************************
21:16:21 
21:16:21 TASK [Gathering Facts] *********************************************************
21:16:21 /usr/local/lib/python3.6/site-packages/ansible/parsing/vault/__init__.py:44: CryptographyDeprecationWarning: Python 3.6 is no longer supported by the Python core team. Therefore, support for it is deprecated in cryptography and will be removed in a future release.
21:16:21   from cryptography.exceptions import InvalidSignature
21:16:22 ok: [instance]
21:16:22 
21:16:22 TASK [Include roles_vector] ****************************************************
21:16:22 
21:16:22 TASK [vector-role : Install vector] *******************************************
21:16:22 included: /opt/jenkins_agent/workspace/vector-role/tasks/install_vector_docker.yml for instance
21:16:22 
21:16:22 TASK [vector-role : VECTOR | Install rpm] *************************************
21:16:32 changed: [instance]
21:16:32 
21:16:32 TASK [vector-role : VECTOR | Template config] *********************************
21:16:33 [WARNING]: The value "0" (type int) was converted to "'0'" (type string). If
21:16:33 this does not look like what you expect, quote the entire value to ensure it
21:16:33 does not change.
21:16:33 changed: [instance]
21:16:33 
21:16:33 TASK [vector-role: Put docker package on hold] *******************************
21:16:34 ok: [instance]
21:16:34 
21:16:34 TASK [vector-role : Install vector] *******************************************
21:16:34 skipping: [instance]
21:16:34 
21:16:34 PLAY RECAP *********************************************************************
21:16:34 instance                   : ok=5    changed=2    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0
21:16:34 
21:16:34 INFO     Running centos_7 > idempotence
21:16:35 
21:16:35 PLAY [Converge] ****************************************************************
21:16:35 
21:16:35 TASK [Gathering Facts] *********************************************************
21:16:35 /usr/local/lib/python3.6/site-packages/ansible/parsing/vault/__init__.py:44: CryptographyDeprecationWarning: Python 3.6 is no longer supported by the Python core team. Therefore, support for it is deprecated in cryptography and will be removed in a future release.
21:16:35   from cryptography.exceptions import InvalidSignature
21:16:36 ok: [instance]
21:16:36 
21:16:36 TASK [Include roles_vector] ****************************************************
21:16:36 
21:16:36 TASK [vector-role : Install vector] *******************************************
21:16:36 included: /opt/jenkins_agent/workspace/vector-role/tasks/install_vector_docker.yml for instance
21:16:36 
21:16:36 TASK [vector-role : VECTOR | Install rpm] *************************************
21:16:41 ok: [instance]
21:16:41 
21:16:41 TASK [vector-role : VECTOR | Template config] *********************************
21:16:42 [WARNING]: The value "0" (type int) was converted to "'0'" (type string). If
21:16:42 this does not look like what you expect, quote the entire value to ensure it
21:16:42 does not change.
21:16:42 ok: [instance]
21:16:42 
21:16:42 TASK [vector-role : Put docker package on hold] *******************************
21:16:43 ok: [instance]
21:16:43 
21:16:43 TASK [vector-role : Install vector] *******************************************
21:16:43 skipping: [instance]
21:16:43 
21:16:43 PLAY RECAP *********************************************************************
21:16:43 instance                   : ok=5    changed=0    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0
21:16:43 
21:16:43 INFO     Idempotence completed successfully.
21:16:43 INFO     Running centos_7 > side_effect
21:16:43 WARNING  Skipping, side effect playbook not configured.
21:16:43 INFO     Running centos_7 > verify
21:16:43 INFO     Running Ansible Verifier
21:16:44 
21:16:44 PLAY [Verify] ******************************************************************
21:16:44 
21:16:44 TASK [Example assertion] *******************************************************
21:16:44 /usr/local/lib/python3.6/site-packages/ansible/parsing/vault/__init__.py:44: CryptographyDeprecationWarning: Python 3.6 is no longer supported by the Python core team. Therefore, support for it is deprecated in cryptography and will be removed in a future release.
21:16:44   from cryptography.exceptions import InvalidSignature
21:16:44 ok: [instance] => {
21:16:44     "changed": false,
21:16:44     "msg": "All assertions passed"
21:16:44 }
21:16:44 
21:16:44 TASK [Check NGINX configs] *****************************************************
21:16:45 changed: [instance]
21:16:45 
21:16:45 TASK [Check NGINX status] ******************************************************
21:16:45 changed: [instance]
21:16:45 
21:16:45 PLAY RECAP *********************************************************************
21:16:45 instance                   : ok=3    changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
21:16:45 
21:16:45 INFO     Verifier completed successfully.
21:16:45 INFO     Running centos_7 > cleanup
21:16:45 WARNING  Skipping, cleanup playbook not configured.
21:16:45 INFO     Running centos_7 > destroy
21:16:46 
21:16:46 PLAY [Destroy] *****************************************************************
21:16:46 
21:16:46 TASK [Destroy molecule instance(s)] ********************************************
21:16:46 /usr/local/lib/python3.6/site-packages/ansible/parsing/vault/__init__.py:44: CryptographyDeprecationWarning: Python 3.6 is no longer supported by the Python core team. Therefore, support for it is deprecated in cryptography and will be removed in a future release.
21:16:46   from cryptography.exceptions import InvalidSignature
21:16:46 changed: [localhost] => (item=instance)
21:16:46 
21:16:46 TASK [Wait for instance(s) deletion to complete] *******************************
21:16:47 FAILED - RETRYING: Wait for instance(s) deletion to complete (300 retries left).
21:16:52 changed: [localhost] => (item=instance)
21:16:52 
21:16:52 TASK [Delete docker networks(s)] ***********************************************
21:16:52 
21:16:52 PLAY RECAP *********************************************************************
21:16:52 localhost                  : ok=2    changed=2    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0
21:16:52 
21:16:52 INFO     Pruning extra files from scenario ephemeral directory
21:16:52 Finished: SUCCESS

```



2. Сделать Declarative Pipeline Job, который будет запускать `molecule test` из любого вашего репозитория с ролью.

<details><summary>Logs</summary>

```
pipeline {
    agent {
        label 'linux'
    }
    stages {
        stage('Git') {
            steps{
                git branch: 'main', credentialsId: '98f5fbb9-b278-47f8-9dc4-16c426ecc1a7', url: 'https://github.com/SemenAmbarnov/vector-role.git'
            }
        }
        stage('Molecule install') {
            steps{
                sh 'pip install molecule==3.4.0'
                sh 'pip install "ansible-lint<6.0.0"'
                sh 'pip install molecule_docker'
            }
        }
        stage('Molecule test'){
            steps{
                sh 'molecule test -s centos7'
                cleanWs()
            }
        }
    }
}
```



3. Перенести Declarative Pipeline в репозиторий в файл `Jenkinsfile`.
4. Создать Multibranch Pipeline на запуск `Jenkinsfile` из репозитория.
5. Создать Scripted Pipeline, наполнить его скриптом из [pipeline](./pipeline).
6. Внести необходимые изменения, чтобы Pipeline запускал `ansible-playbook` без флагов `--check --diff`, если не установлен параметр при запуске джобы (prod_run = True). По умолчанию параметр имеет значение False и запускает прогон с флагами `--check --diff`.
7. Проверить работоспособность, исправить ошибки, исправленный Pipeline вложить в репозиторий в файл `ScriptedJenkinsfile`.
8. Отправить ссылку на репозиторий с ролью и Declarative Pipeline и Scripted Pipeline.
