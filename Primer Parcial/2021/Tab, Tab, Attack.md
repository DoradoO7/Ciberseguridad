## Objetivos
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/9689f2b453ad5daeb73ca7534e4d1521/Addadshashanammu.zip)
## Solucion
rado07-picoctf@webshell:~$ ls
Addadshashanammu  Addadshashanammu.zip  README.txt
dorado07-picoctf@webshell:~$ cd 
.local/           Addadshashanammu/ 
dorado07-picoctf@webshell:~$ cd Addadshashanammu/
dorado07-picoctf@webshell:~/Addadshashanammu$ ls
Almurbalarammi
dorado07-picoctf@webshell:~/Addadshashanammu$ cd Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
dorado07-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet
dorado07-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ chmod +x fang-of-haynekhtnamet 
dorado07-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet
dorado07-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet 
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_2bcfb2ab}
dorado07-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabita
shpi/Maelkashishi/Onnissiralis/Ularradallaku$ 

## Referencias
usando el shell de pico
usaremos el comadno unzip para descomprimir el zip
usaremos el comadno wget para descargar
