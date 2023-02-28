# Level 27 al 28
## Objetivos
There is a git repository at `ssh://bandit27-git@localhost/home/bandit27-git/repo`. The password for the user `bandit27-git` is the same as for the user `bandit27`.

## datos de acceso
bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
## Solucion
```bash
bandit27@bandit:/tmp/tmp.NY6nZh3zWb$ git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
Cloning into 'repo'...
The authenticity of host

bandit27@bandit:/tmp/tmp.NY6nZh3zWb$ ls -la
total 112
drwx------    3 bandit27 bandit27   4096 Feb 28 15:12 .
drwxrwx-wt 2815 root     root     106496 Feb 28 15:13 ..
drwxrwxr-x    3 bandit27 bandit27   4096 Feb 28 15:12 repo
bandit27@bandit:/tmp/tmp.NY6nZh3zWb$ ls
repo
bandit27@bandit:/tmp/tmp.NY6nZh3zWb$ cat repo
cat: repo: Is a directory
bandit27@bandit:/tmp/tmp.NY6nZh3zWb$ ls
repo
bandit27@bandit:/tmp/tmp.NY6nZh3zWb$ cat repo/
cat: repo/: Is a directory
bandit27@bandit:/tmp/tmp.NY6nZh3zWb$ cd repo/
bandit27@bandit:/tmp/tmp.NY6nZh3zWb/repo$ ls
README
bandit27@bandit:/tmp/tmp.NY6nZh3zWb/repo$ cat
.git/   README
bandit27@bandit:/tmp/tmp.NY6nZh3zWb/repo$ cat
.git/   README
bandit27@bandit:/tmp/tmp.NY6nZh3zWb/repo$ cat README
The password to the next level is: AVanL161y9rsbcJIsFHuw35rjaOM19nR
bandit27@bandit:/tmp/tmp.NY6nZh3zWb/repo$

```
## Notas adicionales
Creamos una carpeta y clonamos un repositorio con la ssh que nos brinda el objetivo, despues ingresamos a la carpeta y leemos el readme que esta, y nos mostrara la contraseña para el siguiente nivel.
## Referencias

