# Common Commands

## run / r 

This command runs your program inside the debugger, often this will print information relevant to 
where the crashed occured if you have not set a breakpoint since the program will simply run 
until it finishes or crashes.  If it crashes you will find te next command quite useful. 

### list / l 

This will list the lines of code near where the program crashed.  This will often give you a good 
idea of where to start looking for errors but it is important to note that this will certainly not always 
show you the lines where the root of the problem lies, and more often than not it will not show 
you the line where the problem actually lies. 
where 
This is equivalent to printing a backtrace from within the program, allowing you to see the call 
stack that led to the program crash.  This is helpful by allowing you to see which functions were 
called in what order to lead to the crash. 
up 
This command simply moves you one step back up the call stack 

### ni /next instruction
 

### p / print VARIABLENAME 

This command has two main uses.  You can use it to print out the whatever the current value of 
a variable is at the time of execution, or you can use it to change the value of a variable that is 
currently in scope while the program is running.  This can be useful in some cases to determine 
if a variable is accidentally uninitialized, set to the incorrect value, etc. 

## b / or break breakpoint LINE# or FUNCTION_NAM




### info proc mapping 
 
shows how processes are mapped while in memory

## Timeless Debugging

gdb 

rr is a highly-perfomant record replay by mozzila

qira (qira.me)


### sighed and unsighned integer
  * demsg
  * integer overflow
  * off by one zero error

## check registers

x/gx $rsp

### quickly check sisev location

x/i $rip

### x/4i rip

show 4 rip instructions

# untill main 
*****  

vmmap is used to show how the memory is lined up 
