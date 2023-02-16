# Bandit Level 2 → Level 3
## Objetivos
The password for the next level is stored in a file called **spaces in this filename** located in the home directory
## datos de acceso
bandi 2
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

## Solucion
```bash
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ pwd
/home/bandit2
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$  cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$

```
## Notas adicionales
cat no puede leer los archivos con espacio ya que solo lo toma como 1

| comando | descripcion |
|------------|-------------|
	| ls |  lista archivos |
| cat | muetsra el contenido de un archivo |
| pdw | muetsra el directorio |
| clear | limpirar la pantalla Ctrl -L |
| whoami | muetsra el usiario actual |


## Referencias
[leer archivos con espacios ](https://linuxhint.com/reference-filename-with-spaces-linux/)


