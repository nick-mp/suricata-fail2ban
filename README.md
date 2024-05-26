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


##### 2. Проведите атаку на подбор пароля для службы SSH:

   ![Task](https://github.com/nick-mp/suricata-fail2ban/blob/main/img/2.png)
`Настройка hydra:`
`создайте два файла: users.txt и pass.txt;`
`в каждой строчке первого файла должны быть имена пользователей, второго — пароли. В нашем случае это могут быть случайные строки, но ради эксперимента можете добавить имя и пароль существующего пользователя.`
   ![Task](https://github.com/nick-mp/suricata-fail2ban/blob/main/img/2-1.png)
   ![Task](https://github.com/nick-mp/suricata-fail2ban/blob/main/img/2-2.png)
`Включение защиты SSH для Fail2Ban: открыть файл /etc/fail2ban/jail.conf, найти секцию ssh,`
   ![Task](https://github.com/nick-mp/suricata-fail2ban/blob/main/img/2-3.png)