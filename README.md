# Домашнее задание к занятию 13.1. «Уязвимости и атаки на информационные системы» - 


------

### Задание 1

Скачайте и установите виртуальную машину Metasploitable: https://sourceforge.net/projects/metasploitable/.

Это типовая ОС для экспериментов в области информационной безопасности, с которой следует начать при анализе уязвимостей.

Просканируйте эту виртуальную машину, используя **nmap**.

Попробуйте найти уязвимости, которым подвержена эта виртуальная машина.

Сами уязвимости можно поискать на сайте https://www.exploit-db.com/.

Для этого нужно в поиске ввести название сетевой службы, обнаруженной на атакуемой машине, и выбрать подходящие по версии уязвимости.

Ответьте на следующие вопросы:

- Какие сетевые службы в ней разрешены?
- Какие уязвимости были вами обнаружены? (список со ссылками: достаточно трёх уязвимостей)
  
*Приведите ответ в свободной форме.*  

Какие сетевые службы в ней разрешены?


PORT    	| STATE 	       |SERVICE               | VERSION
----------------|----------------------|----------------------|----------------------
21/tcp   	|open  	               |ftp                   | vsftpd 2.3.4
22/tcp   	|open  		       |ssh                   | OpenSSH 4.7p1 Debian 8ubuntu1 (protocol 2.0)
23/tcp  	| open  	       |telnet                |   Linux telnetd
25/tcp  	| open  	       |smtp                  |   Postfix smtpd
53/tcp  	| open  	       |domain                |   ISC BIND 9.4.2
80/tcp  	| open  	       |http                  |Apache httpd 2.2.8 ((Ubuntu) DAV/2)
111/tcp  	|open  	               |rpcbind               |2 (RPC #100000)
139/tcp  	|open                  |netbios-ssn           |Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
445/tcp  	|open                  |netbios-ssn           |Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
512/tcp  	|open                  | exec                 |netkit-rsh rexecd
513/tcp  	|open                  |login                 | OpenBSD or Solaris rlogind
514/tcp  	|open                  |tcpwrapped            |
1099/tcp 	|open                  |java-rmi              | GNU Classpath grmiregistry
1524/tcp 	|open                  | bindshell            | Metasploitable root shell
2049/tcp 	|open                  | nfs                  |  2-4 (RPC #100003)
2121/tcp 	|open                  |ftp                   | ProFTPD 1.3.1
3306/tcp 	|open                  |mysql                 | MySQL 5.0.51a-3ubuntu5
5432/tcp 	|open                  |postgresql            |PostgreSQL DB 8.3.0 - 8.3.7
5900/tcp 	|open                  | vnc                  | VNC (protocol 3.3)
6000/tcp 	|open                  |X11                   |(access denied)
6667/tcp 	|open                  |irc                   | UnrealIRCd
8009/tcp 	|open                  |ajp13                 | Apache Jserv (Protocol v1.3)
8180/tcp 	|open                  |http                  |Apache Tomcat/Coyote JSP engine 1.1




Какие уязвимости были вами обнаружены? (список со ссылками: достаточно трёх уязвимостей)
 
* https://www.exploit-db.com/exploits/49757 
* https://www.exploit-db.com/exploits/49908 
* https://www.exploit-db.com/exploits/46813 
	



### Задание 2

Проведите сканирование Metasploitable в режимах SYN, FIN, Xmas, UDP.

Запишите сеансы сканирования в Wireshark.

Ответьте на следующие вопросы:

- Чем отличаются эти режимы сканирования с точки зрения сетевого трафика?
- Как отвечает сервер?

*Приведите ответ в свободной форме.*
