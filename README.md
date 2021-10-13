08-ansible-02-playbook

Задание: https://github.com/VitalyMozhaev/mnt-homeworks/tree/main/08-ansible-02-playbook

# Playbook для установки Elasticsearch и Kibana

## Groups_vars

1. all

```text
java_jdk_version - Версия Java JDK (11.0.12)
java_oracle_jdk_package - Файл архива Java JDK (необходимо предварительно скачать!)
```

2. elasticsearch

```text
elastic_version - версия Elasticsearch (7.10.1)
elastic_home - расположение домашнего каталога Elasticsearch
```

3. kibana

```text
kibana_version - версия Kibana (7.10.1)
kibana_home - расположение домашнего каталога Kibana
```

## Inventory

```text
prod.yml - хосты и параметры подключения
```

## Play site.yml

```text
Play описывает поэтапное (tasks) выполнение действий для установки Java JDK, Elasticsearch и Kibana на хосты из выбранного Inventory
```

# Для запуска:

```text
ansible-playbook site.yml -i inventory/prod.yml
```

PS: Пришлось устанавливать локально на одну и туже виртуалку localhost, т.к. создавать другие виртуалки и контейнеры, к сожалению, не было возможности.
