# "Домашнее задание к занятию «Уязвимости и атаки на информационные системы»" - Жаринов Павел

### Задание 1

Открыты следующие порты служб:

  PORT     STATE SERVICE
* 21/tcp   open  ftp
* 22/tcp   open  ssh
* 23/tcp   open  telnet
* 25/tcp   open  smtp
* 53/tcp   open  domain
* 80/tcp   open  http
* 111/tcp  open  rpcbind
* 139/tcp  open  netbios-ssn
* 445/tcp  open  microsoft-ds
* 512/tcp  open  exec
* 513/tcp  open  login
* 514/tcp  open  shell
* 1099/tcp open  rmiregistry
* 1524/tcp open  ingreslock
* 2049/tcp open  nfs
* 2121/tcp open  ccproxy-ftp
* 3306/tcp open  mysql
* 5432/tcp open  postgresql
* 5900/tcp open  vnc
* 6000/tcp open  X11
* 6667/tcp open  irc
* 8009/tcp open  ajp13
* 8180/tcp open  unknown

Перечень обнаруженных уязвимостей (3):
1. [vsftpd 2.3.4 - Backdoor Command Execution](https://www.exploit-db.com/exploits/49757). 
2. [OpenSSH < 7.7 - User Enumeration (2)](https://www.exploit-db.com/exploits/45939). 
3. [MySQL 5.0.x - IF Query Handling Remote Denial of Service](https://www.exploit-db.com/exploits/30020).

---
### Задание 2

Провел сканирование nmap Metasploitable в режимах SYN, FIN, Xmas, UDP

Записи сеансов сканирования в Wireshark
- [nmap-SYN.pcapng](https://github.com/zharinovpy/sdb/blob/main/nmap-SYN.pcapng)
- [nmap-FIN.pcapng](https://github.com/zharinovpy/sdb/blob/main/nmap-FIN.pcapng)
- [nmap-XMAS.pcapng](https://github.com/zharinovpy/sdb/blob/main/nmap-XMAS.pcapng)
- [nmap-UDP.pcapng](https://github.com/zharinovpy/sdb/blob/main/nmap-UDP.pcapng)

Ответьте на следующие вопросы:

- Чем отличаются эти режимы сканирования с точки зрения сетевого трафика?
- Как отвечает сервер?

*Приведите ответ в свободной форме.*

- С точки зрения сетевого трафика эти режимы отличаются типами используемых протоколов передачи и применяемыми флагами в заголовках. 
- Сервер отвечает подтверждением (при доступности порта) или отказом (при недоступности порта), определяя таким образом возможные точки входа.
---
