# Bandit Level 4 → Level 5
## Objetivos
The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.
## datos de acceso
bandit 3
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
## Solucion
```bash
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ ls
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ file ./-file*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ cat -file7
cat: invalid option -- 'f'
Try 'cat --help' for more information.
bandit4@bandit:~/inhere$ cat -file07
cat: invalid option -- 'f'
Try 'cat --help' for more information.
bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
bandit4@bandit:~/inhere$
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
| file* | nos permite buscar en todo |

## Referencias

