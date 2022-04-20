cmdlets are object oriented
Get-command and Get help are you best friends

Get-command 

 Get-Help displays information about a _cmdlet_

search files in powershell using
C:\Users> Get-ChildItem -Path C:\ -Include *interesting-file* -File  -Recurse -ErrorAction SilentlyContinue

Get-Command | ForEach-Object -Begin {$count = 0} -Process{$_ +1} -End{"--- count:$count"}