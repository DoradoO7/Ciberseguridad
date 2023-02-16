# Bandit Level 6 → Level 7
## Objetivos
The password for the next level is stored **somewhere on the server** and has all of the following properties:
-   owned by user bandit7
-   owned by group bandit6
-   33 bytes in size
## datos de acceso
bandit5
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

## Solucion
```bash
bandit6@bandit:~$ ls
bandit6@bandit:~$ ls -la
total 20
drwxr-xr-x  2 root root 4096 Jan 11 19:18 .
drwxr-xr-x 70 root root 4096 Jan 11 19:19 ..
-rw-r--r--  1 root root  220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root root 3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root root  807 Jan  6  2022 .profile
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:~$
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
2>/dev/null nos permiten que los comandos del dispositivo error null sean omitidos 


## Referencias
[Remover el permiso denegado](https://askubuntu.com/questions/350208/what-does-2-dev-null-mean)

