# Ansible playbook Vector-Clickhouse-Lighthouse

### Назначение плэйбука:

[Данный](https://github.com/baldin-lex/08-ansible-03-yandex/tree/main/playbook) плэйбук предназначен для создания системы, способной собирать логи из Вашего приложения, передавать их в СУБД и отображать.

### Состав плэйбука:

1. [Непосредственно, сам плэйбук](https://github.com/baldin-lex/08-ansible-03-yandex/blob/main/playbook/site.yml)
2. [Переменные](https://github.com/baldin-lex/08-ansible-03-yandex/blob/main/playbook/group_vars)
3. [Статический Inventory.](https://github.com/baldin-lex/08-ansible-03-yandex/blob/main/playbook/inventory/prod.yml)
4. [Шаблоны настроек](https://github.com/baldin-lex/08-ansible-03-yandex/blob/main/playbook/templates)

### Подготовка:

*В качестве целевых хостов используются три виртуальные машины в `YC` на базе `CentOS_7`. При использовании данного плэйбука, отредактируйте данный [Inventory-файл](https://github.com/baldin-lex/08-ansible-03-yandex/blob/main/playbook/inventory/prod.yml) в соответствии с Вашей инфраструктурой*

*Конфигурирование Vector, Clickhouse, Lighthouse, а также Nginx осуществляется путем копирования данных [шаблонов](https://github.com/baldin-lex/08-ansible-03-yandex/blob/main/playbook/templates) на целевые хосты. При необходимости внесения изменений в настройки приложений, внесите правки [здесь](https://github.com/baldin-lex/08-ansible-03-yandex/blob/main/playbook/templates)*

*Все переменные, используемые в проекте, находятся [тут](https://github.com/baldin-lex/08-ansible-03-yandex/blob/main/playbook/group_vars)*

### Работа плэйбука:

*После запуска плэйбука, он скачает rpm-пакеты приложений на указанные в Inventory хосты и скопирует на них подготовленные шаблоны настроек.*
