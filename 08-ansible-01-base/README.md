# Домашнее задание к занятию 1 «Введение в Ansible»

## Подготовка к выполнению

1. Установите Ansible версии 2.10 или выше.
2. Создайте свой публичный репозиторий на GitHub с произвольным именем.
3. Скачайте [Playbook](./playbook/) из репозитория с домашним заданием и перенесите его в свой репозиторий.

Решение: Выполнено

## Основная часть

1. Попробуйте запустить playbook на окружении из `test.yml`, зафиксируйте значение, которое имеет факт `some_fact` для указанного хоста при выполнении playbook.

![image](https://user-images.githubusercontent.com/92155007/233993375-d11f90a9-56e5-4980-8724-2dec5060eeb4.png)

2. Найдите файл с переменными (group_vars), в котором задаётся найденное в первом пункте значение, и поменяйте его на `all default fact`.

![image](https://user-images.githubusercontent.com/92155007/233993635-b00ec7e4-5964-427c-821e-701fa82147bf.png)

3. Воспользуйтесь подготовленным (используется `docker`) или создайте собственное окружение для проведения дальнейших испытаний.

![Screenshot from 2023-04-27 16-51-50](https://user-images.githubusercontent.com/92155007/234867387-e34d706e-0f1d-47ae-913d-e3f8ef53302d.png)

4. Проведите запуск playbook на окружении из `prod.yml`. Зафиксируйте полученные значения `some_fact` для каждого из `managed host`.

![image](https://user-images.githubusercontent.com/92155007/234867865-d9f22a54-39f1-42de-8b8f-100c1ad7998c.png)

5. Добавьте факты в `group_vars` каждой из групп хостов так, чтобы для `some_fact` получились значения: для `deb` — `deb default fact`, для `el` — `el default fact`.

Сделано.

6.  Повторите запуск playbook на окружении `prod.yml`. Убедитесь, что выдаются корректные значения для всех хостов.

![Screenshot from 2023-04-27 16-57-09](https://user-images.githubusercontent.com/92155007/234868712-f3f25f3f-b130-471d-b02d-3f9847eff749.png)

7. При помощи `ansible-vault` зашифруйте факты в `group_vars/deb` и `group_vars/el` с паролем `netology`

![image](https://user-images.githubusercontent.com/92155007/234885346-7d0fbad7-09bc-4057-8647-b128a58c7c5b.png)

8. Запустите playbook на окружении `prod.yml`. При запуске `ansible` должен запросить у вас пароль. Убедитесь в работоспособности.

![image](https://user-images.githubusercontent.com/92155007/235100650-7babb6e4-3211-429b-970e-5b85e7ba7996.png)

9. Посмотрите при помощи `ansible-doc` список плагинов для подключения. Выберите подходящий для работы на `control node`.

community.docker.docker_container_info

10. В `prod.yml` добавьте новую группу хостов с именем  `local`, в ней разместите localhost с необходимым типом подключения.

![image](https://user-images.githubusercontent.com/92155007/235116011-e775de25-5e40-4a20-8b6d-7a159321faec.png)

11. Запустите playbook на окружении `prod.yml`. При запуске `ansible` должен запросить у вас пароль. Убедитесь, что факты `some_fact` для каждого из хостов определены из верных `group_vars`.

![image](https://user-images.githubusercontent.com/92155007/235116161-1286d616-481d-482e-bcd7-ec4bb925e1c9.png)

12. Заполните `README.md` ответами на вопросы. Сделайте `git push` в ветку `master`. В ответе отправьте ссылку на ваш открытый репозиторий с изменённым `playbook` и заполненным `README.md`.




