# Level 1
## Objetivos
The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.
## datos de acceso
SSH Information  
Host: bandit.labs.overthewire.org  
Port: 2220
## Solucion
````
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
bandit0@bandit:~$

```
 ````
## Notas adicionales
| comando | descripcion |
|------------|-------------|
	| ls |  lista archivos |
| cat | muetsra el contenido de un archivo |
| pdw | muetsra el directorio |
| clear | limpirar la pantalla Ctrl -L |
| whoami | muetsra el usiario actual |

## Referencias 

