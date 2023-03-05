Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/51/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/51/level1.flag.txt.enc) in the same directory too.
## Solucion

dorado07-picoctf@webshell:~$ ls
Addadshashanammu  README.txt  level2.flag.txt.enc  level2.py
dorado07-picoctf@webshell:~$ cat level2.py 
THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT 
def str_xor(secret, key):
extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
dorado07-picoctf@webshell:~$ python level2.py 
Please enter correct password for flag: 4ec9
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}
dorado07-picoctf@webshell:~$ 

## Referencias
usando el shell de pico 
usaremos wget oara descargar python de scirp
usaremos el comando cat y nos fiaremos en donde diga user 
cat del level2
usaremos python para cuadno leamos metamos y trasformemos los char
