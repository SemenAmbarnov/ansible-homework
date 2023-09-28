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
![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/df9169c2-5ba7-46da-9c2f-83a6c73f28c3)
![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/f29227fc-a8ad-41a8-9420-298bae0dc0c6)
![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/199f20be-770f-4a3d-b50f-b5d2ba70f7f2)
![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/19638ad8-037c-42c7-a4eb-8ec9a3f3452a)

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
*** WARNING: Service runner-atkn1sx-project-57-concurrent-0-81d68747b58428a0-docker-0 probably didn't start properly.
Health check error:
service "runner-atkn1sx-project-57-concurrent-0-81d68747b58428a0-docker-0-wait-for-service" timeout
Health check container logs:
Service container logs:
2023-09-28T08:17:11.326011269Z Generating RSA private key, 4096 bit long modulus (2 primes)
2023-09-28T08:17:12.740628422Z ..............................................................................................................................................++++
2023-09-28T08:17:14.005027354Z .................................................................................................................................++++
2023-09-28T08:17:14.006017841Z e is 65537 (0x010001)
2023-09-28T08:17:14.038965637Z Generating RSA private key, 4096 bit long modulus (2 primes)
2023-09-28T08:17:14.267959636Z .....................++++
2023-09-28T08:17:14.780040805Z ..................................................++++
2023-09-28T08:17:14.780983598Z e is 65537 (0x010001)
2023-09-28T08:17:14.841031820Z Signature ok
2023-09-28T08:17:14.841056069Z subject=CN = docker:dind server
2023-09-28T08:17:14.841206448Z Getting CA Private Key
2023-09-28T08:17:14.867663233Z /certs/server/cert.pem: OK
2023-09-28T08:17:14.871797633Z Generating RSA private key, 4096 bit long modulus (2 primes)
2023-09-28T08:17:15.266550780Z ......................................++++
2023-09-28T08:17:16.665919356Z .............................................................................................................................................++++
2023-09-28T08:17:16.666849739Z e is 65537 (0x010001)
2023-09-28T08:17:16.717468635Z Signature ok
2023-09-28T08:17:16.717505324Z subject=CN = docker:dind client
2023-09-28T08:17:16.717714646Z Getting CA Private Key
2023-09-28T08:17:16.746469504Z /certs/client/cert.pem: OK
2023-09-28T08:17:16.802684708Z time="2023-09-28T08:17:16.802442689Z" level=info msg="Starting up"
2023-09-28T08:17:16.804598191Z time="2023-09-28T08:17:16.804470258Z" level=warning msg="could not change group /var/run/docker.sock to docker: group docker not found"
2023-09-28T08:17:16.804739560Z failed to load listeners: can't create unix socket /var/run/docker.sock: device or resource busy
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
Checking out 3422781d as main...
Skipping Git submodules setup
Executing "step_script" stage of the job script
00:03
Using docker image sha256:1588477122de4fdfe9fcb9ddeeee6ac6b93e9e05a65c68a6e22add0a98b8e0fe for docker:20.10.5 with digest docker@sha256:7ed427295687586039ff3433bb9b4419c5cf1e6294025dadf7641126665a78f5 ...
$ docker build -t $CI_REGISTRY/semen/netology/hello:gitlab-$CI_COMMIT_SHORT_SHA .
#2 [internal] load .dockerignore
#2 sha256:426d8676076bad7882cb0ddbd6d1ac744876e5eddb4c8d55048e47979509c21f
#2 transferring context: 2B done
#2 DONE 0.0s
#1 [internal] load build definition from Dockerfile
#1 sha256:6a0c02bad559058ae521b23b1e784d1df7cbb5dfab3d93584965fb076fe40b2e
#1 transferring dockerfile: 257B done
#1 DONE 0.0s
#3 [internal] load metadata for docker.io/library/centos:7
#3 sha256:30875b35a89c8e8a29cd7cf120689bb68cdab8d769419707e07138dfe977d237
#3 DONE 0.4s
#9 [1/6] FROM docker.io/library/centos:7@sha256:be65f488b7764ad3638f236b7b515b3678369a5124c47b8d32916d6487418ea4
#9 sha256:8aee2df8eae94a334b616b2360efaff20c8e0722b9e9251907e0264f86e84fe1
#9 DONE 0.0s
#7 [internal] load build context
#7 sha256:45ff1ccb41300db1f46c2908e155d62c6f4836fb46c9498b64b4d51bfaf0d360
#7 transferring context: 553B done
#7 DONE 0.0s
#4 [5/6] COPY /python_api/app.py /python_api/app.py
#4 sha256:8c9f2d509ef7f0e819fd60710e7eea0786ad37365016a63edbde7d517ae93598
#4 CACHED
#6 [3/6] COPY requirements.txt requirements.txt
#6 sha256:3aa0f939e237210d6673b7f55dffeb4dfcac9648e42f71a20180f33f635b2b2e
#6 CACHED
#8 [2/6] RUN yum install python3 python3-pip -y
#8 sha256:f1144206e2c393ce7dae78da202bcabe051960e4ee53a33abc414e5f30a9c4cd
#8 CACHED
#5 [4/6] RUN pip3 install -r requirements.txt
#5 sha256:02b69637d62b104831a36ff1260d22b7dfea6bdeedf6f4aafe7e0098c046b42c
#5 CACHED
#10 [6/6] WORKDIR python_api
#10 sha256:25f475072d85666161dd28cc7216240d9ad0a95ba08b37d3985362c227d83156
#10 CACHED
#11 exporting to image
#11 sha256:0e270da4016bad3d718b2a46f02cb72ef26462c32312d3c6e6aa3fdffd5d01d4
#11 exporting layers done
#11 writing image sha256:cda62445480ffc84a1e9d19e8dfa54e583de5b7b9041c07e68e2d0cbd5683de6 done
#11 naming to 192.168.103.44:5005/semen/netology/hello:gitlab-3422781d done
#11 DONE 0.0s
$ docker login -u $CI_REGISTRY_USER -p $CI_REGISTRY_PASSWORD $CI_REGISTRY
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /root/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store
Login Succeeded
$ docker push $CI_REGISTRY/semen/netology/hello:gitlab-$CI_COMMIT_SHORT_SHA
The push refers to repository [192.168.103.44:5005/semen/netology/hello]
5f70bf18a086: Preparing
3c6df952ff76: Preparing
ada6682943e3: Preparing
2f453ee60677: Preparing
f2a815b0a7b6: Preparing
174f56854903: Preparing
174f56854903: Waiting
5f70bf18a086: Mounted from semen/netology/python-api
2f453ee60677: Mounted from semen/netology/python-api
ada6682943e3: Mounted from semen/netology/python-api
f2a815b0a7b6: Mounted from semen/netology/python-api
3c6df952ff76: Mounted from semen/netology/python-api
174f56854903: Mounted from semen/netology/python-api
gitlab-3422781d: digest: sha256:77c196776ee23114ae7e9f669351a83e7953b992d114b0e25be4b9daad57b7bb size: 1572
Job succeeded
```
</details>




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
