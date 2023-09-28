### DevOps

В репозитории содержится код проекта на Python. Проект — RESTful API сервис. Ваша задача — автоматизировать сборку образа с выполнением python-скрипта:

1. Образ собирается на основе [centos:7](https://hub.docker.com/_/centos?tab=tags&page=1&ordering=last_updated).
2. Python версии не ниже 3.7.
3. Установлены зависимости: `flask` `flask-jsonpify` `flask-restful`.
4. Создана директория `/python_api`.
5. Скрипт из репозитория размещён в /python_api.
6. Точка вызова: запуск скрипта.
7. При комите в любую ветку должен собираться docker image с форматом имени hello:gitlab-$CI_COMMIT_SHORT_SHA . Образ должен быть выложен в Gitlab registry или yandex registry.   
8.* (задание необязательное к выполению) При комите в ветку master после сборки должен подняться pod в kubernetes. Примерный pipeline для push в kubernetes по [ссылке](https://github.com/awertoss/devops-netology/blob/main/09-ci-06-gitlab/gitlab-ci.yml).
Если вы еще не знакомы с k8s - автоматизируйте сборку и деплой приложения в docker на виртуальной машине.

# Домашнее задание к занятию 12 «GitLab»

## Основная часть

### DevOps

В репозитории содержится код проекта на Python. Проект — RESTful API сервис. Ваша задача — автоматизировать сборку образа с выполнением python-скрипта:

1. Образ собирается на основе [centos:7](https://hub.docker.com/_/centos?tab=tags&page=1&ordering=last_updated).
2. Python версии не ниже 3.7.
3. Установлены зависимости: `flask` `flask-jsonpify` `flask-restful`.
4. Создана директория `/python_api`.
5. Скрипт из репозитория размещён в /python_api.
6. Точка вызова: запуск скрипта.
7. При комите в любую ветку должен собираться docker image с форматом имени hello:gitlab-$CI_COMMIT_SHORT_SHA . Образ должен быть выложен в Gitlab registry или yandex registry.   
8.* (задание необязательное к выполению) При комите в ветку master после сборки должен подняться pod в kubernetes. Примерный pipeline для push в kubernetes по [ссылке](https://github.com/awertoss/devops-netology/blob/main/09-ci-06-gitlab/gitlab-ci.yml).
Если вы еще не знакомы с k8s - автоматизируйте сборку и деплой приложения в docker на виртуальной машине.

### Для тестов использовал гитлаб с работы. Запускал на shared раннере dind. Переменные прописывал непосредственно в окружении проекта.

![image](https://github.com/SemenAmbarnov/mnt-homeworks/assets/92155007/e11e2c93-8832-40cd-a473-9cee09bcac90)
![image](https://github.com/SemenAmbarnov/mnt-homeworks/assets/92155007/9939dbaa-57c2-44ee-8838-94c8f4f7c26f)
![image](https://github.com/SemenAmbarnov/mnt-homeworks/assets/92155007/1abb186d-ceca-4771-93c8-c0a360fa2bd3)
![image](https://github.com/SemenAmbarnov/mnt-homeworks/assets/92155007/b9d8dc2b-ebe0-4bd6-9770-4bde85e38e3e)

<details><summary>Logs</summary>
  
```
Running with gitlab-runner 15.3.0 (bbcb5aba)
  on sargitlabrunner-docker-in-docker _atKN1Sx
Preparing the "docker" executor
00:36
Using Docker executor with image docker:20.10.5 ...
Starting service docker:20.10.5-dind ...
Pulling docker image docker:20.10.5-dind ...
Using docker image sha256:0a9822c8848df3eb0a1562e553fdd54215939ef0a528434ee026c64ff645148c for docker:20.10.5-dind with digest docker@sha256:e4ecd4e9ad5140d584669451b05e406d8cf7603e51972b862178ad93c38b2b08 ...
WARNING: Service docker:20.10.5-dind is already created. Ignoring.
Waiting for services to be up and running (timeout 30 seconds)...
*** WARNING: Service runner-atkn1sx-project-57-concurrent-0-4b0b90b62c516efa-docker-0 probably didn't start properly.
Health check error:
service "runner-atkn1sx-project-57-concurrent-0-4b0b90b62c516efa-docker-0-wait-for-service" timeout
Health check container logs:
Service container logs:
2023-09-28T07:48:47.438114360Z Generating RSA private key, 4096 bit long modulus (2 primes)
2023-09-28T07:48:47.472678714Z .++++
2023-09-28T07:48:47.860786227Z ....................................++++
2023-09-28T07:48:47.861708792Z e is 65537 (0x010001)
2023-09-28T07:48:47.891327557Z Generating RSA private key, 4096 bit long modulus (2 primes)
2023-09-28T07:48:48.179517701Z ...........................++++
2023-09-28T07:48:48.576754467Z ......................................++++
2023-09-28T07:48:48.577736183Z e is 65537 (0x010001)
2023-09-28T07:48:48.630786361Z Signature ok
2023-09-28T07:48:48.631814218Z subject=CN = docker:dind server
2023-09-28T07:48:48.632195224Z Getting CA Private Key
2023-09-28T07:48:48.659458291Z /certs/server/cert.pem: OK
2023-09-28T07:48:48.666148330Z Generating RSA private key, 4096 bit long modulus (2 primes)
2023-09-28T07:48:51.032241125Z ................................................................................................................................................................................................................................................++++
2023-09-28T07:48:51.603549603Z ........................................................++++
2023-09-28T07:48:51.604359508Z e is 65537 (0x010001)
2023-09-28T07:48:51.651502048Z Signature ok
2023-09-28T07:48:51.651543352Z subject=CN = docker:dind client
2023-09-28T07:48:51.651767148Z Getting CA Private Key
2023-09-28T07:48:51.679289396Z /certs/client/cert.pem: OK
2023-09-28T07:48:51.729979274Z time="2023-09-28T07:48:51.729771541Z" level=info msg="Starting up"
2023-09-28T07:48:51.732157047Z time="2023-09-28T07:48:51.732038525Z" level=warning msg="could not change group /var/run/docker.sock to docker: group docker not found"
2023-09-28T07:48:51.732336415Z failed to load listeners: can't create unix socket /var/run/docker.sock: device or resource busy
*********
Pulling docker image docker:20.10.5 ...
Using docker image sha256:1588477122de4fdfe9fcb9ddeeee6ac6b93e9e05a65c68a6e22add0a98b8e0fe for docker:20.10.5 with digest docker@sha256:7ed427295687586039ff3433bb9b4419c5cf1e6294025dadf7641126665a78f5 ...
Preparing environment
00:00
Running on runner-atkn1sx-project-57-concurrent-0 via gitlab...
Getting source from Git repository
00:01
Fetching changes with git depth set to 20...
Reinitialized existing Git repository in /builds/semen/netology/.git/
Checking out e8b3434e as main...
Skipping Git submodules setup
Executing "step_script" stage of the job script
01:56
Using docker image sha256:1588477122de4fdfe9fcb9ddeeee6ac6b93e9e05a65c68a6e22add0a98b8e0fe for docker:20.10.5 with digest docker@sha256:7ed427295687586039ff3433bb9b4419c5cf1e6294025dadf7641126665a78f5 ...
$ docker build -t $CI_REGISTRY/semen/netology/python-api:latest .
#1 [internal] load build definition from Dockerfile
#1 sha256:069dcef77f108770a23a777a71c32095e370a7238243ad1b812153f729825d22
#1 transferring dockerfile: 257B done
#1 DONE 0.0s
#2 [internal] load .dockerignore
#2 sha256:eee716ffcc3309abe5863bd3bfaef44f8046808832f0114ed3ae75d0147ad50a
#2 transferring context: 2B done
#2 DONE 0.0s
#3 [internal] load metadata for docker.io/library/centos:7
#3 sha256:30875b35a89c8e8a29cd7cf120689bb68cdab8d769419707e07138dfe977d237
#3 DONE 1.0s
#4 [internal] load build context
#4 sha256:4ca0672e948ffbffbf2676846fe5b329f901a7a786e0a2c6539960a9d9b2631a
#4 transferring context: 553B done
#4 DONE 0.0s
#6 [1/6] FROM docker.io/library/centos:7@sha256:be65f488b7764ad3638f236b7b515b3678369a5124c47b8d32916d6487418ea4
#6 sha256:8aee2df8eae94a334b616b2360efaff20c8e0722b9e9251907e0264f86e84fe1
#6 resolve docker.io/library/centos:7@sha256:be65f488b7764ad3638f236b7b515b3678369a5124c47b8d32916d6487418ea4 done
#6 sha256:be65f488b7764ad3638f236b7b515b3678369a5124c47b8d32916d6487418ea4 1.20kB / 1.20kB done
#6 sha256:dead07b4d8ed7e29e98de0f4504d87e8880d4347859d839686a31da35a3b532f 529B / 529B done
#6 sha256:eeb6ee3f44bd0b5103bb561b4c16bcb82328cfe5809ab675bb17ab3a16c517c9 2.75kB / 2.75kB done
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 0B / 76.10MB 0.2s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 4.19MB / 76.10MB 1.4s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 8.39MB / 76.10MB 3.1s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 12.58MB / 76.10MB 5.0s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 16.78MB / 76.10MB 6.9s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 20.97MB / 76.10MB 9.1s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 25.17MB / 76.10MB 11.6s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 29.36MB / 76.10MB 13.3s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 33.55MB / 76.10MB 15.0s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 37.75MB / 76.10MB 17.0s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 41.94MB / 76.10MB 19.0s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 46.14MB / 76.10MB 21.1s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 50.33MB / 76.10MB 23.0s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 54.53MB / 76.10MB 25.0s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 58.72MB / 76.10MB 27.1s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 62.91MB / 76.10MB 28.9s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 67.11MB / 76.10MB 30.5s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 71.30MB / 76.10MB 32.5s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 75.50MB / 76.10MB 34.2s
#6 sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 76.10MB / 76.10MB 34.8s done
#6 extracting sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc
#6 extracting sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 5.1s
#6 extracting sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc 7.8s done
#6 DONE 43.0s
#5 [2/6] RUN yum install python3 python3-pip -y
#5 sha256:f1144206e2c393ce7dae78da202bcabe051960e4ee53a33abc414e5f30a9c4cd
#5 0.640 Loaded plugins: fastestmirror, ovl
#5 0.827 Determining fastest mirrors
#5 6.356  * base: mirror.sale-dedic.com
#5 6.356  * extras: mirror.sale-dedic.com
#5 6.357  * updates: mirror.sale-dedic.com
#5 27.27 Resolving Dependencies
#5 27.27 --> Running transaction check
#5 27.27 ---> Package python3.x86_64 0:3.6.8-19.el7_9 will be installed
#5 27.28 --> Processing Dependency: python3-libs(x86-64) = 3.6.8-19.el7_9 for package: python3-3.6.8-19.el7_9.x86_64
#5 27.63 --> Processing Dependency: python3-setuptools for package: python3-3.6.8-19.el7_9.x86_64
#5 27.63 --> Processing Dependency: libpython3.6m.so.1.0()(64bit) for package: python3-3.6.8-19.el7_9.x86_64
#5 27.63 ---> Package python3-pip.noarch 0:9.0.3-8.el7 will be installed
#5 27.63 --> Running transaction check
#5 27.63 ---> Package python3-libs.x86_64 0:3.6.8-19.el7_9 will be installed
#5 27.65 --> Processing Dependency: libtirpc.so.1()(64bit) for package: python3-libs-3.6.8-19.el7_9.x86_64
#5 27.65 ---> Package python3-setuptools.noarch 0:39.2.0-10.el7 will be installed
#5 27.65 --> Running transaction check
#5 27.65 ---> Package libtirpc.x86_64 0:0.2.4-0.16.el7 will be installed
#5 27.81 --> Finished Dependency Resolution
#5 27.81 
#5 27.81 Dependencies Resolved
#5 27.82 
#5 27.82 ================================================================================
#5 27.82  Package                  Arch         Version              Repository     Size
#5 27.82 ================================================================================
#5 27.82 Installing:
#5 27.82  python3                  x86_64       3.6.8-19.el7_9       updates        70 k
#5 27.82  python3-pip              noarch       9.0.3-8.el7          base          1.6 M
#5 27.82 Installing for dependencies:
#5 27.82  libtirpc                 x86_64       0.2.4-0.16.el7       base           89 k
#5 27.82  python3-libs             x86_64       3.6.8-19.el7_9       updates       6.9 M
#5 27.82  python3-setuptools       noarch       39.2.0-10.el7        base          629 k
#5 27.82 
#5 27.82 Transaction Summary
#5 27.82 ================================================================================
#5 27.82 Install  2 Packages (+3 Dependent packages)
#5 27.82 
#5 27.82 Total download size: 9.3 M
#5 27.82 Installed size: 48 M
#5 27.82 Downloading packages:
#5 27.92 warning: /var/cache/yum/x86_64/7/updates/packages/python3-3.6.8-19.el7_9.x86_64.rpm: Header V4 RSA/SHA256 Signature, key ID f4a80eb5: NOKEY
#5 27.92 Public key for python3-3.6.8-19.el7_9.x86_64.rpm is not installed
#5 27.94 Public key for libtirpc-0.2.4-0.16.el7.x86_64.rpm is not installed
#5 36.01 --------------------------------------------------------------------------------
#5 36.01 Total                                              1.1 MB/s | 9.3 MB  00:08     
#5 36.01 Retrieving key from file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
#5 36.02 Importing GPG key 0xF4A80EB5:
#5 36.02  Userid     : "CentOS-7 Key (CentOS 7 Official Signing Key) <security@centos.org>"
#5 36.02  Fingerprint: 6341 ab27 53d7 8a78 a7c2 7bb1 24c6 a8a7 f4a8 0eb5
#5 36.02  Package    : centos-release-7-9.2009.0.el7.centos.x86_64 (@CentOS)
#5 36.02  From       : /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
#5 36.04 Running transaction check
#5 36.06 Running transaction test
#5 36.13 Transaction test succeeded
#5 36.13 Running transaction
#5 36.23   Installing : libtirpc-0.2.4-0.16.el7.x86_64                               1/5 
#5 37.20   Installing : python3-setuptools-39.2.0-10.el7.noarch                      2/5 
#5 37.67   Installing : python3-pip-9.0.3-8.el7.noarch                               3/5 
#5 37.71   Installing : python3-3.6.8-19.el7_9.x86_64                                4/5 
#5 39.37   Installing : python3-libs-3.6.8-19.el7_9.x86_64                           5/5 
#5 39.43   Verifying  : libtirpc-0.2.4-0.16.el7.x86_64                               1/5 
#5 39.44   Verifying  : python3-libs-3.6.8-19.el7_9.x86_64                           2/5 
#5 39.45   Verifying  : python3-3.6.8-19.el7_9.x86_64                                3/5 
#5 39.46   Verifying  : python3-setuptools-39.2.0-10.el7.noarch                      4/5 
#5 39.47   Verifying  : python3-pip-9.0.3-8.el7.noarch                               5/5 
#5 39.51 
#5 39.51 Installed:
#5 39.51   python3.x86_64 0:3.6.8-19.el7_9        python3-pip.noarch 0:9.0.3-8.el7       
#5 39.51 
#5 39.51 Dependency Installed:
#5 39.51   libtirpc.x86_64 0:0.2.4-0.16.el7                                              
#5 39.51   python3-libs.x86_64 0:3.6.8-19.el7_9                                          
#5 39.51   python3-setuptools.noarch 0:39.2.0-10.el7                                     
#5 39.51 
#5 39.51 Complete!
#5 DONE 40.3s
#10 [3/6] COPY requirements.txt requirements.txt
#10 sha256:8a567cb26318172b1bd59e947643adf79cd47b55093c84bed723edb6f85240ed
#10 DONE 0.3s
#9 [4/6] RUN pip3 install -r requirements.txt
#9 sha256:5a263187caaca86b48124e80e2792e0114159d8db0c09a39f13ad53500d645aa
#9 0.823 WARNING: Running pip install with root privileges is generally not a good idea. Try `pip3 install --user` instead.
#9 0.897 Collecting flask (from -r requirements.txt (line 1))
#9 1.583   Downloading https://files.pythonhosted.org/packages/cd/77/59df23681f4fd19b7cbbb5e92484d46ad587554f5d490f33ef907e456132/Flask-2.0.3-py3-none-any.whl (95kB)
#9 1.764 Collecting flask-restful (from -r requirements.txt (line 2))
#9 2.081   Downloading https://files.pythonhosted.org/packages/d7/7b/f0b45f0df7d2978e5ae51804bb5939b7897b2ace24306009da0cc34d8d1f/Flask_RESTful-0.3.10-py2.py3-none-any.whl
#9 2.205 Collecting flask_jsonpify (from -r requirements.txt (line 3))
#9 2.543   Downloading https://files.pythonhosted.org/packages/60/0f/c389dea3988bffbe32c1a667989914b1cc0bce31b338c8da844d5e42b503/Flask-Jsonpify-1.5.0.tar.gz
#9 3.090 Collecting itsdangerous>=2.0 (from flask->-r requirements.txt (line 1))
#9 3.359   Downloading https://files.pythonhosted.org/packages/9c/96/26f935afba9cd6140216da5add223a0c465b99d0f112b68a4ca426441019/itsdangerous-2.0.1-py3-none-any.whl
#9 3.465 Collecting Jinja2>=3.0 (from flask->-r requirements.txt (line 1))
#9 3.744   Downloading https://files.pythonhosted.org/packages/20/9a/e5d9ec41927401e41aea8af6d16e78b5e612bca4699d417f646a9610a076/Jinja2-3.0.3-py3-none-any.whl (133kB)
#9 3.886 Collecting click>=7.1.2 (from flask->-r requirements.txt (line 1))
#9 4.184   Downloading https://files.pythonhosted.org/packages/4a/a8/0b2ced25639fb20cc1c9784de90a8c25f9504a7f18cd8b5397bd61696d7d/click-8.0.4-py3-none-any.whl (97kB)
#9 4.311 Collecting Werkzeug>=2.0 (from flask->-r requirements.txt (line 1))
#9 4.641   Downloading https://files.pythonhosted.org/packages/f4/f3/22afbdb20cc4654b10c98043414a14057cd27fdba9d4ae61cea596000ba2/Werkzeug-2.0.3-py3-none-any.whl (289kB)
#9 4.838 Collecting pytz (from flask-restful->-r requirements.txt (line 2))
#9 5.369   Downloading https://files.pythonhosted.org/packages/32/4d/aaf7eff5deb402fd9a24a1449a8119f00d74ae9c2efa79f8ef9994261fc2/pytz-2023.3.post1-py2.py3-none-any.whl (502kB)
#9 5.730 Collecting six>=1.3.0 (from flask-restful->-r requirements.txt (line 2))
#9 5.991   Downloading https://files.pythonhosted.org/packages/d9/5a/e7c31adbe875f2abbb91bd84cf2dc52d792b5a01506781dbcf25c91daf11/six-1.16.0-py2.py3-none-any.whl
#9 6.093 Collecting aniso8601>=0.82 (from flask-restful->-r requirements.txt (line 2))
#9 6.362   Downloading https://files.pythonhosted.org/packages/e3/04/e97c12dc034791d7b504860acfcdd2963fa21ae61eaca1c9d31245f812c3/aniso8601-9.0.1-py2.py3-none-any.whl (52kB)
#9 6.510 Collecting MarkupSafe>=2.0 (from Jinja2>=3.0->flask->-r requirements.txt (line 1))
#9 7.010   Downloading https://files.pythonhosted.org/packages/fc/d6/57f9a97e56447a1e340f8574836d3b636e2c14de304943836bd645fa9c7e/MarkupSafe-2.0.1-cp36-cp36m-manylinux1_x86_64.whl
#9 7.118 Collecting importlib-metadata; python_version < "3.8" (from click>=7.1.2->flask->-r requirements.txt (line 1))
#9 7.549   Downloading https://files.pythonhosted.org/packages/a0/a1/b153a0a4caf7a7e3f15c2cd56c7702e2cf3d89b1b359d1f1c5e59d68f4ce/importlib_metadata-4.8.3-py3-none-any.whl
#9 7.695 Collecting dataclasses; python_version < "3.7" (from Werkzeug>=2.0->flask->-r requirements.txt (line 1))
#9 7.947   Downloading https://files.pythonhosted.org/packages/fe/ca/75fac5856ab5cfa51bbbcefa250182e50441074fdc3f803f6e76451fab43/dataclasses-0.8-py3-none-any.whl
#9 8.050 Collecting zipp>=0.5 (from importlib-metadata; python_version < "3.8"->click>=7.1.2->flask->-r requirements.txt (line 1))
#9 8.354   Downloading https://files.pythonhosted.org/packages/bd/df/d4a4974a3e3957fd1c1fa3082366d7fff6e428ddb55f074bf64876f8e8ad/zipp-3.6.0-py3-none-any.whl
#9 8.483 Collecting typing-extensions>=3.6.4; python_version < "3.8" (from importlib-metadata; python_version < "3.8"->click>=7.1.2->flask->-r requirements.txt (line 1))
#9 8.786   Downloading https://files.pythonhosted.org/packages/45/6b/44f7f8f1e110027cf88956b59f2fad776cca7e1704396d043f89effd3a0e/typing_extensions-4.1.1-py3-none-any.whl
#9 8.844 Installing collected packages: itsdangerous, MarkupSafe, Jinja2, zipp, typing-extensions, importlib-metadata, click, dataclasses, Werkzeug, flask, pytz, six, aniso8601, flask-restful, flask-jsonpify
#9 9.927   Running setup.py install for flask-jsonpify: started
#9 10.35     Running setup.py install for flask-jsonpify: finished with status 'done'
#9 10.44 Successfully installed Jinja2-3.0.3 MarkupSafe-2.0.1 Werkzeug-2.0.3 aniso8601-9.0.1 click-8.0.4 dataclasses-0.8 flask-2.0.3 flask-jsonpify-1.5.0 flask-restful-0.3.10 importlib-metadata-4.8.3 itsdangerous-2.0.1 pytz-2023.3.post1 six-1.16.0 typing-extensions-4.1.1 zipp-3.6.0
#9 DONE 11.0s
#8 [5/6] COPY /python_api/app.py /python_api/app.py
#8 sha256:47daba8b25637f4e0253478cff7b8a5b7bcad1ba60fed05f26722ec2a6a7a1f9
#8 DONE 0.0s
#7 [6/6] WORKDIR python_api
#7 sha256:bde9ad88a85ccec75109964d012ea286a274ab279bfcab19bc87a1210cc3549f
#7 DONE 0.0s
#11 exporting to image
#11 sha256:172151d817bc372a3ffc77cdfcca5220a55039590f0c61b92475708666fe4467
#11 exporting layers
#11 exporting layers 3.0s done
#11 writing image sha256:cda62445480ffc84a1e9d19e8dfa54e583de5b7b9041c07e68e2d0cbd5683de6 done
#11 naming to 192.168.103.44:5005/semen/netology/python-api:latest done
#11 DONE 3.0s
$ docker login -u $CI_REGISTRY_USER -p $CI_REGISTRY_PASSWORD $CI_REGISTRY
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /root/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store
Login Succeeded
$ docker push $CI_REGISTRY/semen/netology/python-api:latest
The push refers to repository [192.168.103.44:5005/semen/netology/python-api]
5f70bf18a086: Preparing
3c6df952ff76: Preparing
ada6682943e3: Preparing
2f453ee60677: Preparing
f2a815b0a7b6: Preparing
174f56854903: Preparing
174f56854903: Waiting
2f453ee60677: Pushed
3c6df952ff76: Pushed
5f70bf18a086: Pushed
ada6682943e3: Pushed
174f56854903: Pushed
f2a815b0a7b6: Pushed
latest: digest: sha256:77c196776ee23114ae7e9f669351a83e7953b992d114b0e25be4b9daad57b7bb size: 1572
Job succeeded
```
</details>

![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/a26c450c-75a1-4aa6-b520-e17252cee09e)


### Product Owner

Вашему проекту нужна бизнесовая доработка: нужно поменять JSON ответа на вызов метода GET `/rest/api/get_info`, необходимо создать Issue в котором указать:

1. Какой метод необходимо исправить.
2. Текст с `{ "message": "Already started" }` на `{ "message": "Running"}`.
3. Issue поставить label: feature.

### Developer

Пришёл новый Issue на доработку, вам нужно:

1. Создать отдельную ветку, связанную с этим Issue.
2. Внести изменения по тексту из задания.
3. Подготовить Merge Request, влить необходимые изменения в `master`, проверить, что сборка прошла успешно.


### Tester

Разработчики выполнили новый Issue, необходимо проверить валидность изменений:

1. Поднять докер-контейнер с образом `python-api:latest` и проверить возврат метода на корректность.
2. Закрыть Issue с комментарием об успешности прохождения, указав желаемый результат и фактически достигнутый.

## Итог

В качестве ответа пришлите подробные скриншоты по каждому пункту задания:

- файл gitlab-ci.yml;
- Dockerfile; 
- лог успешного выполнения пайплайна;
- решённый Issue.

### Важно 
После выполнения задания выключите и удалите все задействованные ресурсы в Yandex Cloud.

## Необязательная часть

Автомазируйте работу тестировщика — пусть у вас будет отдельный конвейер, который автоматически поднимает контейнер в docker или k8s и выполняет проверку, например, при помощи curl. На основе вывода будет приниматься решение об успешности прохождения тестирования.



### Product Owner

Вашему проекту нужна бизнесовая доработка: нужно поменять JSON ответа на вызов метода GET `/rest/api/get_info`, необходимо создать Issue в котором указать:

1. Какой метод необходимо исправить.
2. Текст с `{ "message": "Already started" }` на `{ "message": "Running"}`.
3. Issue поставить label: feature.

### Developer

Пришёл новый Issue на доработку, вам нужно:

1. Создать отдельную ветку, связанную с этим Issue.
2. Внести изменения по тексту из задания.
3. Подготовить Merge Request, влить необходимые изменения в `master`, проверить, что сборка прошла успешно.


### Tester

Разработчики выполнили новый Issue, необходимо проверить валидность изменений:

1. Поднять докер-контейнер с образом `python-api:latest` и проверить возврат метода на корректность.
2. Закрыть Issue с комментарием об успешности прохождения, указав желаемый результат и фактически достигнутый.

## Итог

В качестве ответа пришлите подробные скриншоты по каждому пункту задания:

- файл gitlab-ci.yml;
- Dockerfile; 
- лог успешного выполнения пайплайна;
- решённый Issue.
