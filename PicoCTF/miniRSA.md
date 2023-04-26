
## Objetivos
Let's decrypt this: [ciphertext](https://jupiter.challenges.picoctf.org/static/d21037ad23ed84cfff20a84768a0f2b2/ciphertext)? Something seems a bit small.
## Solucion
Descargaremos el archivo que nos proporciona la pagina y luego al abrirlo solo usaremmos el valor que se nos asigno en el ciphertext 
despues crearemos un prorama que nos ayude usando ayudas ya que tienen python 
from gmpy2 import *
from Crypto.Util.number import long_to_bytes

gmpy2.get_context().precision=2048

e = 3
c = 2205316413931134031074603746928247799030155221252519872650073010782049179856976080512716237308882294226369300412719995904064931819531456392957957122459640736424089744772221933500860936331459280832211445548332429338572369823704784625368933 

root, exact= iroot(c,e)

print( long_to_bytes(root))

## Referencias
[Video](https://www.youtube.com/watch?v=-csder3s3ZU)