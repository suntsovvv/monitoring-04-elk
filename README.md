
# Домашнее задание к занятию 15 «Система сбора логов Elastic Stack»

## Задание 1

Вам необходимо поднять в докере и связать между собой:

- elasticsearch (hot и warm ноды);
- logstash;
- kibana;
- filebeat.

Logstash следует сконфигурировать для приёма по tcp json-сообщений.

Filebeat следует сконфигурировать для отправки логов docker вашей системы в logstash.

В директории [help](./help) находится манифест docker-compose и конфигурации filebeat/logstash для быстрого 
выполнения этого задания.

Результатом выполнения задания должны быть:

- скриншот `docker ps` через 5 минут после старта всех контейнеров (их должно быть 5);
![image](https://github.com/suntsovvv/monitoring-04-elk/assets/154943765/7f3a62e9-94f6-416b-87ec-63980cdd48d9)

- скриншот интерфейса kibana;
![image](https://github.com/suntsovvv/monitoring-04-elk/assets/154943765/b7686d04-8717-465a-bec0-4631a2769012)


## Задание 2

Перейдите в меню [создания index-patterns  в kibana](http://localhost:5601/app/management/kibana/indexPatterns/create) и создайте несколько index-patterns из имеющихся.   

![image](https://github.com/suntsovvv/monitoring-04-elk/assets/154943765/84aa6b12-6e47-4371-890b-196b601c3372)

Перейдите в меню просмотра логов в kibana (Discover) и самостоятельно изучите, как отображаются логи и как производить поиск по логам.   
![image](https://github.com/suntsovvv/monitoring-04-elk/assets/154943765/52626cef-0067-43cf-a2bb-5b009998967d)


В манифесте директории help также приведенно dummy-приложение, которое генерирует рандомные события в stdout-контейнера.
Эти логи должны порождать индекс logstash-* в elasticsearch. Если этого индекса нет — воспользуйтесь советами и источниками из раздела «Дополнительные ссылки» этого задания.   
![image](https://github.com/suntsovvv/monitoring-04-elk/assets/154943765/d6176cbc-d12c-41a9-874b-997ac12008a3)

 
---


 
