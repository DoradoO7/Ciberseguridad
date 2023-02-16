#  Bandit Level 3 → Level 4
## Objetivos
The password for the next level is stored in a hidden file in the **inhere** directory.
## datos de acceso
bandit 3 
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
## Solucion
```bash 

bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ pwd
/home/bandit3
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ find
.
./.hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
bandit3@bandit:~/inhere$
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



## Referencias


