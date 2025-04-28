# Ansible

## Task 3

### Разворачивание стека мониторинга

- Возьмите в работу плейбук [monitoring_project](https://github.com/lamjob1993/ansible-monitoring/blob/main/ansible/monitoring_project/playbook.yml):
  - Возьмите в работу две OS: Debian и CentOS
  - При этом:
    - Grafana, Prometheus, Alertmanager, Nginx и PostgreSQL должны быть развернуты Unit-файлами на CentOS на пяти отдельных VM
    - Node Exporter, Process Exporter и Blackbox Exporter должны быть развернуты Unit-файлами на Debian на трех отдельных VM
    - Node Exporter же, как отдельный инстанс от всех должен стоять на всех восьми VM: Debian + CentOS
  - Подумайте как распределить железо по VM-кам (советую: 2 CPU + 1Гб RAM + 10Гб HDD)
  - С помощью Terraform нарежьте 8 операционок через один скрипт
  - Выведите получившуюся картину на дашборды:
    - Дашборды использовать официальные
    - 8 инстансов Node Exporter-ов должны вызываться из одной переменной в Grafana
    - На каждый уникальный инстанс вывести уникальный и официальный дашборд
  - Запушьте изменения в GitHub
