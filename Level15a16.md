# Level 15 a 16

## Objetivo
	The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**
## Datos de acceso
	Usuario: bandit15
	Contraseña: BfMYroe26WYalil77FoDi9qh59eK5xNr
## Solución
	bandit15@bandit:~$ openssl s_client -connect localhost:30001
	CONNECTED(00000003)
	depth=0 CN = localhost
	verify error:num=18:self signed certificate
	verify return:1
	depth=0 CN = localhost
	verify return:1
	---
	Certificate chain
	 0 s:/CN=localhost
	   i:/CN=localhost
	---
	Server certificate
	
	
	    Start Time: 1661868694
	    Timeout   : 7200 (sec)
	    Verify return code: 18 (self signed certificate)
	    Extended master secret: yes
	---
	BfMYroe26WYalil77FoDi9qh59eK5xNr
	Correct!
	cluFn7wTiGryunymYOu4RcffSxQluehd
	
	closed
## Notas adicionales
	 Utilizaremos el comando: openssl s_client -connect localhost:30001
	 El localhost le indicamos el puerto que el objetivo nos indica, que es donde se encuentra la contraseña, para poder obtenerla solamente debemos poner la contraseña de este usuario (15). 
## Referencias 