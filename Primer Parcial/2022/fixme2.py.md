## Objetivos
Fix the syntax error in this Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/38/fixme1.py)
## Solucion

dorado07-picoctf@webshell:~$ ls
Addadshashanammu  code.py       convertme.py  fixme2.py
README.txt        codebook.txt  fixme1.py     runme.py
dorado07-picoctf@webshell:~$ python fixme2.py 
  File "/home/dorado07-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
dorado07-picoctf@webshell:~$ nano fixme2.py 
dorado07-picoctf@webshell:~$ python fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
dorado07-picoctf@webshell:~$ 


## Referencias
usando el shell de pico 
usaremos wget oara descargar python de scirp
Correjiremos la sintaxis del archivo con la ayuda de nano

