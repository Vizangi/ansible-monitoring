# Ansible

## Task 3

### Автоматизируем деплой стека мониторинга на VM

- Возьмите в работу плейбук [monitoring_project](https://github.com/lamjob1993/ansible-monitoring/blob/main/ansible/monitoring_project/playbook.yml) (в комментариях подсказка):
  - Возьмите в работу две OS:
    - **Debian Minimal** (только терминал)
    - **CentOS Minimal** (только терминал)
  - С помощью **Terraform** нарежьте 8 операционок через один скрипт (это обязательно)
  - Подумайте как распределить железо по VM-кам (минимально на x1 VM: 2 CPU + 768Мб RAM + 10Гб SSD)
  - Напишите [основной плейбук](https://github.com/lamjob1993/ansible-monitoring/blob/main/ansible/monitoring_project/playbook.yml), наполните файл [инвентори](https://github.com/lamjob1993/ansible-monitoring/blob/main/ansible/monitoring_project/inventory.ini) и роли на стек ниже и задеплойте:
    - Grafana, Prometheus, Alertmanager, Nginx и PostgreSQL должны быть развернуты Unit-файлами на **CentOS на пяти отдельных VM**
    - Process Exporter и Blackbox Exporter должны быть развернуты Unit-файлами на **Debian на двух отдельных VM**
    - Node Exporter (+ x1 Debian, которой не хватает с голым Node Exporter) должен стоять **на всех восьми VM** сразу: микс из **Debian** + **CentOS**
  - Выведите получившуюся картину на дашборды:
    - Дашборды использовать официальные (они у вас уже были скачаны по [Docker репозиторию](https://github.com/lamjob1993/docker-monitoring/blob/main/docker/task_4.md))
    - На каждый уникальный инстанс вывести уникальный и официальный дашборд
    - Все 8 инстансов **Node Exporter-ов** на дашборде **Node Exporter Full** должны вызываться из одной переменной в **Grafana**
  - Запушьте изменения в GitHub
