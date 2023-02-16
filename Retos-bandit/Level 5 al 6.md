#  Bandit Level 5 → Level 6
## Objetivos
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:
-   human-readable
-   1033 bytes in size
-   not executable
## datos de acceso
bandit 4
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
## Solucion
```bash
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
bandit5@bandit:~/inhere$ find . -readable -type f -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
                                                                                                                                                    
```

## Notas adicionales
| comando | descripcion |
|------------|-------------|
	| ls |  lista archivos |
| cat | muetsra el contenido de un archivo |
| pdw | muetsra el directorio |
| clear | limpirar la pantalla Ctrl -L |
| whoami | muetsra el usiario actual |
| cd | nos permite movernos  de directorio |
| find | Nos permite buscar |
| -readble | que el archivo sea legible |
| -type | el tipo del archivo |
| -size | el tamañño que queremos |
mand find 
/ readable - buscar la palaba redeable dentro del manual de ayudda
-N -buscar la siguiente ocurrencia hacia adelante
-n - busca la siguiente ocurrencia hacia atras 
-q -salir del manual de ayuda 




## Referencias
