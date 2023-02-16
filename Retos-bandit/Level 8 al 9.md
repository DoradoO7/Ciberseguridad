# Bandit Level 8 → Level 9
## Objetivos
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
## datos de acceso
bandit 7
TESKZC0XvTetK0S9xNwm25STk5iWrBvP

## Solucion
```bash
bandit8@bandit:~$
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ wc data.txt
 1001  1001 33033 data.txt
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$

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
		|uniq | filtra los repetidos
		| c | cuenta |
		
		
## Referencias

[comado wc](https://explainshell.com/explain?cmd=wc)
