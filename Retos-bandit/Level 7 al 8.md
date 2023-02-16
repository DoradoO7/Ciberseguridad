# Bandit Level 7 → Level 8
## Objetivos
The password for the next level is stored in the file **data.txt** next to the word **millionth**

## datos de acceso
bandit 6
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

## Solucion

```bash
bandit7@bandit:~$
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ wc data.txt
  98567  197133 4184396 data.txt
bandit7@bandit:~$ grep millionth data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$ cat data.txt | grep millionth
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$
bandit7@bandit:~$

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
|grep | print lines matching a pattern|


## Referencias

[buscador de comandos](https://explainshell.com/explain?cmd=grep)
[concidencias en archivos](https://www.geeksforgeeks.org/grep-command-in-unixlinux/?ref=rp)
