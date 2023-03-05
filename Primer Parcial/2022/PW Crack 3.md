## Objetivos
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/24/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/24/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/24/level3.hash.bin) in the same directory too. There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solucion
dorado07-picoctf@webshell:~$ python pwhash.py 
  File "/home/dorado07-picoctf/pwhash.py", line 16
    print(i)
TabError: inconsistent use of tabs and spaces in indentation
dorado07-picoctf@webshell:~$ nano pwhash.py
dorado07-picoctf@webshell:~$ python pwhash.py 
dba8
dorado07-picoctf@webshell:~$ pytho level3.py 
-bash: pytho: command not found
dorado07-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: dba8
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
dorado07-picoctf@webshell:~$ 

## Referencias
usando el shell de pico 
usaremos wget oara descargar python de scirp
usaremos nano para crear un programa en python el cual nos de la clave del level 3

