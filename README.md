# ETP.SAMPLE.1C

Работа с IBM WebsphereMQ происходит через COM объект MQAX200

Официальная документация: https://www.ibm.com/support/knowledgecenter/en/SSFKSJ_7.5.0/com.ibm.mq.dev.doc/q033320_.htm

Перед началом работы необходимо установить параметры подключения к серверу с помощью переменной окружения MQSERVER
```sh
MQSERVER=CLIENT.SVRCONN/TCP/127.0.0.1(2424)
```
Примеры записи сообщения в очередь и чтения сообщения из очереди находятся в файле 1С_WebsphereMQ_samples.1C исходный код приведен для системы 1С:Предприятие версии 8.0 и выше.

Также для работы необходима библиотека MQAX200.dll если у вас не установлен локально WebsphereMQ

Ниже инструкция установки библиотеки для разных версий операционных систем.

Шаг 1: Определите тип своей операционной системы 32 bit/64 bit

Шаг 2: Скопируйте dll файл MQAX200.dll в следующие директории:
```sh
32 bit : %systemroot%\system32\XXXXXX.dll
64 bit : %systemroot%\sysWOW64\XXXXXX.dll
```

Пример: 
```sh
32 bit : C:\Windows\system32\MQAX200.dll
64 bit : C:\Windows\sysWOW64\MQAX200.dll
```

Шаг 3 : Выполните в консоли следующие команды от имени администратора
```sh
32 bit : regsvr32 "C:\Windows\system32\MQAX200.dll"
64 bit : regsvr32  "C:\Windows\sysWOW64\MQAX200.dll"
```
		 
Шаг 4: Должно появится следующее сообщение
```sh
DllRegisterServer in C:\Windows\SysWOW64\mqax200.dll succeeded.
```


Шаг 5: Если вы получили следующую ошибку
```sh
The module "C:\Windows\System32\mqax200.dll" failed to load. Make sure the binary is stored at the specified path or debug it to check for problems with the binary or dependent .DLL files. The specified module could not be found
```
Решение:
1) Проверьте действительно ли вы поместили файл mqax200.dll в нужную директорию
2) Необходимы права администратора
3) Проверьте разрядность системы и разрядность библиотек
