# Level 12 al 13
## Objetivos
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## datos de acceso
bandit12
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
## Solucion
```bash
bandit12@bandit:~$ ls
data.txt
bandit12@bandit:~$ xxd -r data.txt | file -
/dev/stdin: gzip compressed data, was "data2.bin", last modified: Wed Jan 11 19:18:38 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt |zcat | file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt |zcat |bzcat |zcat | file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt |zcat |bzcat |zcat | tar x0 | file -
tar: Options '-[0-7][lmh]' not supported by *this* tar
Try 'tar --help' or 'tar --usage' for more information.
/dev/stdin: empty
bandit12@bandit:~$ xxd -r data.txt |zcat |bzcat |zcat | tar x0 | file -
tar: Options '-[0-7][lmh]' not supported by *this* tar
Try 'tar --help' or 'tar --usage' for more information.
/dev/stdin: empty
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat |file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | file -
/dev/stdin: gzip compressed data, was "data9.bin", last modified: Wed Jan 11 19:18:38 2023, max compression, from Unix
bandit12@bandit:~$
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat | file -
/dev/stdin: ASCII text
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
bandit12@bandit:~$
```
## Notas adicionales
| comando | descripcion |
|------------|-------------|
	| ls |  lista archivos |
| cat | muetsra el contenido de un archivo |
| echo | display a line of text |
| base64 | base64 encode/decode data and print to standard output|
| tr | translate or delete characters|

| ext| comp |desc| ver consola |
|------------|-------------|---------|------|----------|
|.gz |gzip |gzip -d |zcat|
|.bz2 |bzip2 |bzop -s |bzcat|
|.tar |tar| tar xf | tar xO|

## Referencias
[Hex dump on Wikipedia](https://en.wikipedia.org/wiki/Hex_dump)
[Ayuda de class](https://ingsoftware.reduaz.mx/moodle/pluginfile.php/68462/mod_resource/content/2/06-retos-bandit-p3.pdf)
