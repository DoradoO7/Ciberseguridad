#  Bandit Level 9 → Level 10
## Objetivos
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
## datos de acceso
bandit 8
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
## Solucion
```bash
bandit9@bandit:~$
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ file data.txt
data.txt: data
bandit9@bandit:~$ strings data.txt | grep ==
c========== the
h;========== password
========== isT
n.E========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit9@bandit:~$
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
		| wc | print newline, word, and byte counts for each file|
| string | print the strings of printable characters in files|

## Referencias
[comando string ](https://explainshell.com/explain?cmd=strings)

