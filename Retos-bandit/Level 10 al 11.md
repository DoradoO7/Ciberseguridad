# Level 10 al 11
## Objetivos
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
## datos de acceso
bandit10
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
## Solucion
```bash
bandit10@bandit:~$
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root     root     4096 Jan 11 19:18 .
drwxr-xr-x 70 root     root     4096 Jan 11 19:19 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit11 bandit10   69 Jan 11 19:18 data.txt
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ echo "hola mundo"
hola mundo
bandit10@bandit:~$ echo "hola mundo" | base64
aG9sYSBtdW5kbwo=
bandit10@bandit:~$ echo -n aG9sYSBtdW5kbwo= | base64 -d
hola mundo
bandit10@bandit:~$ base64 -d data.txt
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$
```
## Notas adicionales
| comando | descripcion |
|------------|-------------|
	| ls |  lista archivos |
| cat | muetsra el contenido de un archivo |
| echo | display a line of text |
| base64 | base64 encode/decode data and print to standard output|
| tr | translate or delete characters|




## Referencias
[Base64 info](https://en.wikipedia.org/wiki/Base64)

