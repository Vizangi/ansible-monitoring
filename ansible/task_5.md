# Ansible

## Task 5

### Проверка состояния ПО на серверах, а также автоматическая установка в случае его отсутствия или перезапуск

- Нужно написать роль, которая сможет на всех VM-ках:
  - Проверить наличие на виртуалке Node Exporter / node_exporter_install_path:
    - Установить Node Exporter (если он отсутствует)
  - Проверить состояние службы Node Exporter:
    - Если не запущена, то запустить: `sudo systemctl start node_exporter.service`
  - Проверить доступность метрик Node Exporter:
    - Скрипт должен заходить на страницу `/metrics`, видеть статус `200 OK` и что метрики отбрасываются / не отбрасываются каждым экспортером
- По [заданию 3](https://github.com/lamjob1993/ansible-monitoring/blob/main/ansible/task_3.md) у вас уже были задеплоены x8 Node Exporter-ов:
  - Сделайте имитацию, что 3 экспортера не запущены `sudo systemctl stop node_exporter.service` и `sudo systemctl disable node_exporter.service`
  - x1 Node Exporter полностью удалите с VM
  - Далее запустите Ansible скрипт и убедитесь в его успешном выполнении
- Запушьте изменения в Github
