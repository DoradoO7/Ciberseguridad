## Objetivos
Class, take your seats! It's PRIME-time for a quiz... `nc jupiter.challenges.picoctf.org 58617`
## Solucion
p=primo 1
q=primo 2
n=modulo
tn= totient n(euler)
e=exponente(llave publica)  2^16+1=65537
d= llave privada
n=p*q
tn=(p-1)*(q-1)
d= e mod inv yn / inverse(e,tn)
Encriptar
C=m^e mod n / pow(m,e,n)
Desencriptar
m=c^d mod n / pow(c,d,n)s
from Crypto.Util.number import *

seguiremos el video 
picoCTF{wA8_th4t$_ill3aGal..o26cefcb2}


## Referencias
[Video](https://www.youtube.com/watch?v=HIwgWauz-fc&t=1259s)
