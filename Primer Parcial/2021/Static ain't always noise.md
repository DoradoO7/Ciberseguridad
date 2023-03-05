## Objetivos
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/static)? This [BASH script](https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/ltdis.sh) might help!
## Solucion
dorado07-picoctf@webshell:~$ ls
README.txt  flag         ltdis.sh  strings    strings.2
file        flagout.txt  static    strings.1  warm
dorado07-picoctf@webshell:~$ chmod +x ltdis.sh 
dorado07-picoctf@webshell:~$ ./ltdis.sh static 
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
dorado07-picoctf@webshell:~$ sta
start-stop-daemon  stat               
dorado07-picoctf@webshell:~$ sttatic.ltdis.strings.txt
-bash: sttatic.ltdis.strings.txt: command not found
dorado07-picoctf@webshell:~$ static.ltdis.strings.txt
-bash: static.ltdis.strings.txt: command not found
dorado07-picoctf@webshell:~$ ls
README.txt  flag         ltdis.sh  static.ltdis.strings.txt  strings    strings.2
file        flagout.txt  static    static.ltdis.x86_64.txt   strings.1  warm
dorado07-picoctf@webshell:~$ static.ltdis.strings.txt
-bash: static.ltdis.strings.txt: command not found
dorado07-picoctf@webshell:~$ cat static.ltdis.strings.txt
    238 /lib64/ld-linux-x86-64.so.2
    361 libc.so.6
    36b puts
    370 __cxa_finalize
    37f __libc_start_main
    391 GLIBC_2.2.5
    39d _ITM_deregisterTMCloneTable
    3b9 __gmon_start__
    3c8 _ITM_registerTMCloneTable
    660 AWAVI
    667 AUATL
    6ba []A\A]A^A_
    6e8 Oh hai! Wait what? A flag? Yes, it's around here somewhere!
    7c7 ;*3$"
   1020 picoCTF{d15a5m_t34s3r_6f8c8200}
## Referencias
usando el shell de pico
Usamos el comando strings para convertir lo que hay en el documento
