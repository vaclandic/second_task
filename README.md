# ELK playbook

Устанавливает Java
Устанавливает и настараивает elasticsearch и kibana

## Запуск:

```bash
ansible-playbook -i inventory/prod.yml site.yml
```
## Используемые тэги:

 - java - установить только Java
 - elastic - установить только Elastic
 - kibana - установить только Kibana


## Переменные:

| Название        | Значение по умолчанию           | Описание  |
| ------------- |:-------------:| -----:|
| java_jdk_version      | 8u281 | Версия Java |
| java_oracle_jdk_package      | jdk-8u281-linux-x64.tar.gz      |   Название пакета Java для установки |
|elastic_version|7.10.1|Версия Elasticsearch|
|elastic_home|/opt/elastic/$elastic_version|Директория куда будет установлен Elasticsearch|
|kibana_version|7.10.1|Версия Kibana|
|kibana_home|/opt/kibana/$kibana_version|Директория куда будет установлена Kibaba|
|kibana_port|5601|Порт, на котором будет слушать Kibana|
|kibana_host|localhost|Адрес, на котором будет слушать Kibana|
|elastic_hosts|["http://localhost:9200"]|Список серверов Elasticsearch, к которым будет подключаться Kibana|