# powershell
#scripting
powershell uses cmdlets
cmdlets are object oriented
Get-command and Get help are you best friends
Get-Help displays information about a _cmdlet_

## Get-command 

 
 
 to

search files in powershell using
C:\Users> Get-ChildItem -Path C:\ -Include *interesting-file* -File  -Recurse -ErrorAction SilentlyContinue

Get-Command | ForEach-Object -Begin {$count = 0} -Process{$_ +1} -End{"--- count:$count"}





learn powershell scripting
[go through]
https://learnxinyminutes.com/docs/powershell/