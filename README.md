# Домашнее задание к занятию «Система мониторинга Zabbix» Шарапат Виктор

### Задание 1 

Установите Zabbix Server с веб-интерфейсом.

#### Процесс выполнения
1. Выполняя ДЗ, сверяйтесь с процессом отражённым в записи лекции.
2. Установите PostgreSQL. Для установки достаточна та версия, что есть в системном репозитороии Debian 11.
3. Пользуясь конфигуратором команд с официального сайта, составьте набор команд для установки последней версии Zabbix с поддержкой PostgreSQL и Apache.
4. Выполните все необходимые команды для установки Zabbix Server и Zabbix Web Server.

#### Требования к результаты 
1. Прикрепите в файл README.md скриншот авторизации в админке.
2. Приложите в файл README.md текст использованных команд в GitHub.

---
### Решение (Задание 1):
Я не много отошёл от процесса выполнения задания и использовал:
1)	Ubuntu 20.04.6 LTS.
2)	Nginx.
3)	Postgresql 14 (т.к. Zabbix Server 6.4 требуется версия не ниже Postgresql 13, можно использовать и ниже версии, предварительно отключи в конфигурации Zabbix-server проверку, но лучше использовать рекомендованные требования).
4)	Расширение Timescaledb (для сжатия базы).
   
Все команды по установке Zabbix Server брал с оф. сайта Zabbix. 

![alt text](https://github.com/sharvik22/sharvik22-zabbix-hw-02/blob/main/images/Screenshot_17.png)

![alt text](https://github.com/sharvik22/sharvik22-zabbix-hw-02/blob/main/images/Screenshot_19.png)

![alt text](https://github.com/sharvik22/sharvik22-zabbix-hw-02/blob/main/images/Screenshot_20.png)

![alt text](https://github.com/sharvik22/sharvik22-zabbix-hw-02/blob/main/images/Screenshot_3.png)

![alt text](https://github.com/sharvik22/sharvik22-zabbix-hw-02/blob/main/images/Screenshot_10.png)


### Задание 2 

Установите Zabbix Agent на два хоста.

#### Процесс выполнения
1. Выполняя ДЗ, сверяйтесь с процессом отражённым в записи лекции.
2. Установите Zabbix Agent на 2 вирт.машины, одной из них может быть ваш Zabbix Server.
3. Добавьте Zabbix Server в список разрешенных серверов ваших Zabbix Agentов.
4. Добавьте Zabbix Agentов в раздел Configuration > Hosts вашего Zabbix Servera.
5. Проверьте, что в разделе Latest Data начали появляться данные с добавленных агентов.

#### Требования к результаты 
1. Приложите в файл README.md скриншот раздела Configuration > Hosts, где видно, что агенты подключены к серверу
2. Приложите в файл README.md скриншот лога zabbix agent, где видно, что он работает с сервером
3. Приложите в файл README.md скриншот раздела Monitoring > Latest data для обоих хостов, где видны поступающие от агентов данные.
4. Приложите в файл README.md текст использованных команд в GitHub

---
### Решение (Задание 2):
![alt text](https://github.com/sharvik22/sharvik22-zabbix-hw-02/blob/main/images/Screenshot_21.png)

![alt text](https://github.com/sharvik22/sharvik22-zabbix-hw-02/blob/main/images/Screenshot_26.png)

![alt text](https://github.com/sharvik22/sharvik22-zabbix-hw-02/blob/main/images/Screenshot_23.png)

![alt text](https://github.com/sharvik22/sharvik22-zabbix-hw-02/blob/main/images/Screenshot_22.png)

![alt text](https://github.com/sharvik22/sharvik22-zabbix-hw-02/blob/main/images/Screenshot_23.png)

Команды по установке и настройке zabbix-agent
1. sudo apt update
2. sudo apt install zabbix-agent
3. sudo nano /etc/zabbix/zabbix_agentd.conf
4. sudo systemctl restart zabbix-agent
5. sudo systemctl enable zabbix-agent
6. sudo systemctl status zabbix-agent


## Задание 3 со звёздочкой*
Установите Zabbix Agent на Windows (компьютер) и подключите его к серверу Zabbix.

#### Требования к результаты 
1. Приложите в файл README.md скриншот раздела Latest Data, где видно свободное место на диске C:
--- 
### Решение (Задание 3):
![alt text](https://github.com/sharvik22/sharvik22-zabbix-hw-02/blob/main/images/Screenshot_25.png)
![alt text](https://github.com/sharvik22/sharvik22-zabbix-hw-02/blob/main/images/Screenshot_21.png)
![alt text](https://github.com/sharvik22/sharvik22-zabbix-hw-02/blob/main/images/Screenshot_27.png)




