# Ansible

## Task 4

_Для подобного рода задач заводится таска в Jira (вкратце в описании описывается план проведения работ, выставляется время проведения работ, указывается исполнитель и ответственный), прикладывается документация в формате `.docx`, где прописано построчно, что будет происходить, и что делать в случае сбоя (откат). То есть вот вам еще одна строчка в резюме - придумайте, как её красиво расписать._

### Пишем пайплайн

#### Автоматизируем деплой стека мониторинга на три контура разработки (dev, stage, prod) по x8 контейнеров (на рабочем проекте в облаке - это будут инстансы)

- На данном этапе мы наблюдаем наглядное представление **Terraform IaC** с [развертыванием инфраструктуры](https://github.com/lamjob1993/terraform-monitoring/blob/main/terraform/tasks/task_4.md) и управлением, как кодом + **Ansible IaC** с развертыванием конфигурации и управлением, как кодом.
- Возьмите в работу плейбук [monitoring_project](https://github.com/lamjob1993/ansible-monitoring/blob/main/ansible/tasks/monitoring_project/playbook.yml) (в комментариях YAML подсказка):
  - Возьмите в работу **Docker**:
    - С помощью **Terraform** уже нарезано три контура по 8 инстансов в каждом [по заданию 4](https://github.com/lamjob1993/terraform-monitoring/blob/main/terraform/tasks/task_4.md) по репозиторию **Terraform**.
  - Напишите основной плейбук, наполните файл [инвентори](https://github.com/lamjob1993/ansible-monitoring/blob/main/ansible/tasks/monitoring_project/inventory.ini) и напишите роли на стек мониторинга из [плейбука](https://github.com/lamjob1993/ansible-monitoring/blob/main/ansible/tasks/monitoring_project/playbook.yml).
  - Еще раз обратите внимание на [пайплайн](https://github.com/lamjob1993/terraform-monitoring/blob/main/terraform/beggining/%D0%9C%D0%BE%D0%B4%D1%83%D0%BB%D1%8C%208%3A%20%D0%9F%D1%80%D0%B8%D0%BC%D0%B5%D1%80%20%D0%BF%D0%B0%D0%B9%D0%BF%D0%BB%D0%B0%D0%B9%D0%BD%D0%B0.md) и какую в нём роль играет **Ansible**.
  - Выведите получившуюся картину на дашборды:
    - Дашборды использовать официальные (они у вас уже были скачаны по [Docker репозиторию](https://github.com/lamjob1993/docker-monitoring/blob/main/docker/tasks/docker_learn/task_4%20(Docker%20Compose%20Plus).md)).
    - На каждый уникальный инстанс вывести уникальный и официальный дашборд.
  - Запушьте изменения в **GitHub**.
