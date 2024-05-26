# "Защита сети" - Горегляд Николай

### Подготовка Подготовка к выполнению заданий

`Подготовка защищаемой системы:`
`    установите Suricata,`
`    установите Fail2Ban.`

`Подготовка системы злоумышленника: установите nmap и thc-hydra либо скачайте и установите Kali linux.`

   ![Task](https://github.com/nick-mp/suricata-fail2ban/blob/main/img/1.png)

##### 1. Проведите разведку системы и определите, какие сетевые службы запущены на защищаемой системе:

`sudo nmap -sA < ip-адрес >`
   ![Task](https://github.com/nick-mp/suricata-fail2ban/blob/main/img/1-1.png)

`sudo nmap -sT < ip-адрес >`
   ![Task](https://github.com/nick-mp/suricata-fail2ban/blob/main/img/1-2.png)

`sudo nmap -sS < ip-адрес >`
   ![Task](https://github.com/nick-mp/suricata-fail2ban/blob/main/img/1-3.png)

`sudo nmap -sV < ip-адрес >`
   ![Task](https://github.com/nick-mp/suricata-fail2ban/blob/main/img/1-4.png)

##### пояснение: Так как проверка проводилась на чистой ubuntu на которой почти ничего не было, то и результатом явился единственный порт 80.


##### 2. Проведите атаку на подбор пароля для службы SSH:

`для проверки атаки по словарю с использованием hydra на ubuntu установлен openssh-server`

   ![Task](https://github.com/nick-mp/suricata-fail2ban/blob/main/img/2.png)

`установлен fail2ban`

   ![Task](https://github.com/nick-mp/suricata-fail2ban/blob/main/img/2-1.png)
   ![Task](https://github.com/nick-mp/suricata-fail2ban/blob/main/img/2-2.png)

`внесены настройки для Fail2Ban в файле /etc/fail2ban/jail.conf`

   ![Task](https://github.com/nick-mp/suricata-fail2ban/blob/main/img/2-3.png)

##### результатом явилось помещение ip-адреса Kali в бан, и возможность перебора логинов и паролей стала недоступна