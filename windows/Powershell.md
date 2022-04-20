# powershell
#scripting
powershell uses cmdlets
cmdlets are object oriented
Get-command and Get help are you best friends
## Get-Help
Get-Help displays information about a _cmdlet_
to get examples use 
Get-Help Get-Command -Examples

## Get-command 
Get comand is used to search for commands
when one types get commands it list all commands

## Get-ChildItem
search files in powershell using
 Get-ChildItem -Path C:\ -Include *interesting-file* -File  -Recurse -ErrorAction SilentlyContinue

Search for all files containing a string eg "API_KEY"

Get-ChildItem C:\* -Recurse | Select-String -pattern API_KEY

## Get-Hotfix
shows windows updates aplied

## Get-Process
lists processes


learn powershell scripting
[go through]
https://learnxinyminutes.com/docs/powershell/