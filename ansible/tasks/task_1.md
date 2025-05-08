# Ansible

## Task 1

### Пишем первую роль и деплоимся на x3 VM

- Познакомьтесь с разделом [monitoring_project](https://github.com/lamjob1993/ansible-monitoring/tree/main/ansible/tasks/monitoring_project):
  - Это рабочий проект **Ansible**
  - У вас по следующим заданиям должен быть такой же
- Попробуйте выстроить логическую цепочку:
  - За что отвечают переменные
  - Зачем нужен инвентори
  - Какие модули задействуются
  - Зачем нужен плейбук
  - Зачем нужны роли
- Установите Ansible на свободную VM из-под бинаря с официального сайта
- Напишите и запустите роль **Process Exporter** сразу на трех VM по аналогии с разделом [monitoring_project](https://github.com/lamjob1993/ansible-monitoring/tree/main/ansible/monitoring_project):
  - Process Exporter ставим `Unit-файлом` со всеми вытекающими
- Проверьте с помощью скрипта Ansible, что **Process Exporter-ы** отдают метрики на `/metrics` и двигайтесь дальше
- Запушьте изменения в GitHub
