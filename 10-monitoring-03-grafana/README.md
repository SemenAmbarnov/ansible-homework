### Задание 1

1. Используя директорию [help](./help) внутри этого домашнего задания, запустите связку prometheus-grafana.
1. Зайдите в веб-интерфейс grafana, используя авторизационные данные, указанные в манифесте docker-compose.
1. Подключите поднятый вами prometheus, как источник данных.
1. Решение домашнего задания — скриншот веб-интерфейса grafana со списком подключенных Datasource.

![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/0a80ca6e-3b33-4c14-bc11-179ca42d6114)


## Задание 2

Изучите самостоятельно ресурсы:

1. [PromQL tutorial for beginners and humans](https://valyala.medium.com/promql-tutorial-for-beginners-9ab455142085).
1. [Understanding Machine CPU usage](https://www.robustperception.io/understanding-machine-cpu-usage).
1. [Introduction to PromQL, the Prometheus query language](https://grafana.com/blog/2020/02/04/introduction-to-promql-the-prometheus-query-language/).

Создайте Dashboard и в ней создайте Panels:

- утилизация CPU для nodeexporter (в процентах, 100-idle);
- CPULA 1/5/15;
- количество свободной оперативной памяти;
- количество места на файловой системе.

Для решения этого задания приведите promql-запросы для выдачи этих метрик, а также скриншот получившейся Dashboard.

CPU Usage 
```
(((count(count(node_cpu_seconds_total{}) by (cpu))) - avg(sum by (mode)(rate(node_cpu_seconds_total{mode='idle'}[$__rate_interval])))) * 100) / count(count(node_cpu_seconds_total{}) by (cpu))
```
Free Memory
```
node_memory_MemFree_bytes
```

Load Average
```
node_load1
node_load5
node_load15
```
Disk Free Space
```
node_filesystem_avail_bytes
```


![image](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/5e468180-20db-47e4-bd12-ede82b6bd935)




## Задание 3

1. Создайте для каждой Dashboard подходящее правило alert — можно обратиться к первой лекции в блоке «Мониторинг».
1. В качестве решения задания приведите скриншот вашей итоговой Dashboard.

![Screenshot from 2023-10-02 15-53-46](https://github.com/SemenAmbarnov/ansible-homework/assets/92155007/a9ab0c27-ff86-4d51-884d-f5cd315956ab)


## Задание 4

1. Сохраните ваш Dashboard.Для этого перейдите в настройки Dashboard, выберите в боковом меню «JSON MODEL». Далее скопируйте отображаемое json-содержимое в отдельный файл и сохраните его.
1. В качестве решения задания приведите листинг этого файла.
