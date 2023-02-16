#  Bandit Level 1 → Level 2
## Objetivos
The password for the next level is stored in a file called **-** located in the home directory
## datos de acceso
bandit 1
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

## Solucion
````bash
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ pwd
/home/bandit1
bandit1@bandit:~$ whoami
bandit1
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$
````

## Notas adicionales
cuando cat ve un - se confunde  la maquina 

| comando | descripcion |
|------------|-------------|
	| ls |  lista archivos |
| cat | muetsra el contenido de un archivo |
| pdw | muetsra el directorio |
| clear | limpirar la pantalla Ctrl -L |
| whoami | muetsra el usiario actual |


## Referencias
[archivos con guiones](https://stackoverflow.com/questions/42187323/how-to-open-a-dashed-filename-using-terminal)



