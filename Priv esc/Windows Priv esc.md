
## if you have admn permission you can then new account using
`net user <username> <password> /add`

`net localgroup administrators <username> /add`

# 1.user accounts levels

-   Administrator (local): This is the user with the most privileges.
-   Standard (local): These users can access the computer but can only perform limited tasks. Typically these users can not make permanent or essential changes to the system. 
-   Guest: This account gives access to the system but is not defined as a user. 
-   Standard (domain): Active Directory allows organizations to manage user accounts. A standard domain account may have local administrator privileges. 
-   Administrator (domain): Could be considered as the most privileged user. It can edit, create, and delete other users throughout the organization's domain.

enumeration scripts like winpeas or powerups.ps1

## 2 The following commands will help us enumerate users and their privileges on the target system.

Current user’s privileges: `whoami /priv`

List users: `net users`

List details of a user: `net user username` (e.g. `net user Administrator`)

Other users logged in simultaneously: `qwinsta` (the `query session` command can be used the same way) 

User groups defined on the system: `net localgroup`

List members of a specific group: `net localgroup groupname` (e.g. `net localgroup Administrators`)


# 3.collecting info

systeminfo | findstr /B /C:"OS Name" /C:"OS Version

# 4. Searching files


The `findstr` command can be used to find such files in a format similar to the one given below:

`findstr /si password *.txt`

Command breakdown:

`findstr`: Searches for patterns of text in files.

`/si`: Searches the current directory and all subdirectories (s), ignores upper case / lower case differences (i)

`password`: The command will search for the string “password” in files

`*.txt`: The search will cover files that have a .txt extension

The string and file extension can be changed according to your needs and the target environment, but “.txt”, “.xml”, “.ini”, “*.config”, and “.xls” are usually a good place to start.

# 5. Patch level

`wmic qfe get Caption,Description,HotFixID,InstalledOn`

## 6.Network Connections
netstat -ano

-   `-a`: Displays all active connections and listening ports on the target system.
-   `-n`: Prevents name resolution. IP Addresses and ports are displayed with numbers instead of attempting to resolves names using DNS.
-   `-o`: Displays the process ID using each listed connection.

## 7.Scheduled Tasks

`schtasks /query /fo LIST /v`

## 8.Drivers
The `driverquery` command will list drivers installed on the target system. You will 
need to do some online research about the drivers listed and see if any presents a potential privilege escalation vulnerability.

## 9.Antivirus

to check for windows defender use 
`sc query windefend`
to check for other solutions use 
`sc queryex type=service`

 [Get-MpComputerStatus](https://docs.microsoft.com/en-us/powershell/module/defender/get-mpcomputerstatus?view=win10-ps)
 
# check software with
wmic product

wmic product get name,version,vendor

wmic service list brief

to get more info on a service use wmic
# dll msfvenom

you cancreat an illegal dll with msfvenom

# cross compile 
this mean compiling c code using linux for a windows system 
you must use windows api though

sudo x86_64-w64-migw32-gcc code.c -shared -o compiled_binary_name.exe




cd:

runs while executing files 


