find / -perm -u=s >/dev/null
find / -perm -u=s -type f 2>/dev/null
 
 privilage escalition 
 
 one can do priv esc using 
 1.kernel exploits  flaws
 2.programs that any user can sudo
 3.programs with setuid bit on
 4.Limited capabilites
 
 ## add + to search for a specific tpe of paylod eg +suid or +sudo
 
 sudo -l
 
 ## Limited Capabilities 
 check if there applications has increased limited capabilites  
 ## you can get root by modifying cron job to perform 
 
 ##find what programs have suid then remove a file they want to run with a file that you have created