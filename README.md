# ETP.SAMPLE.1C

Работа с IBM WebsphereMQ происходит через COM объект MQAX200

Первым делом необходимо установить клиент IBM MQ 7.5.0.4: http://www-01.ibm.com/software/integration/wmq/clients/

Официальная документация: https://www.ibm.com/support/knowledgecenter/en/SSFKSJ_7.5.0/com.ibm.mq.dev.doc/q033320_.htm

Перед началом работы необходимо установить параметры подключения к серверу с помощью переменной окружения MQSERVER
```sh
MQSERVER=CLIENT.SVRCONN/TCP/127.0.0.1(2424)
```
Примеры записи сообщения в очередь и чтения сообщения из очереди находятся в файле 1С_WebsphereMQ_samples.1C исходный код приведен для системы 1С:Предприятие версии 8.0 и выше.

Добавлен пример обработки для 1С Предприятие 8.3
```sh
1С_IBMMQ.epf
```
