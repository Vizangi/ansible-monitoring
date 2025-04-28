# Ansible

## Task 1

- Познакомьтесь с разделом [monitoring_project](https://github.com/lamjob1993/ansible-monitoring/tree/main/ansible/monitoring_project):
  - Это рабочий проект Ansible
  - У вас по следующим заданиям должен быть такой же
- Попробуйте выстроить логическую цепочку:
  - За что отвечают переменные
  - Зачем нужен инвентори
  - Какие модули задействуются
  - Зачем нужен плейбук
  - Зачем нужны роли
- Установите Ansible на свободную VM из-под бинаря с официального сайта (Ansible должен стоять на самостоятельной (отдельной от остальных) VM)
- Напишите и запустите роль Process Exporter на трех VM одновременно по аналогии с разделом [monitoring_project](https://github.com/lamjob1993/ansible-monitoring/tree/main/ansible/monitoring_project)
  - Process Exporter ставим Unit-файлом со всеми вытекающими
- Проверьте, что Process Exporter-ы отдают метрики на `/metrics` и двигайтесь дальше
- Запушьте изменения в GitHub
