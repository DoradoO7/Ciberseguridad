

## Descripcion
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message.Download the corrupted message [here](https://artifacts.picoctf.net/c/192/message.txt).
## Pistas
- Split the message up into blocks of 3 and see how the first block is scrambled
## Solucion
```
MESSAGE="heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V9AAB1F8}7"

FLAG=""
for i in range(0,len(MESSAGE),3):

	FLAG +=MESSAGE[i+2] + MESSAGE[i:i+2]

print(FLAG)

se crearra un pequeño programa el cual nos ayude a rotaarlo hasta que nos de el mensaje de forma entendible 
```

## Bandera

picoCTF{7R4N5P051N6_15_3XP3N51V3_A9AFB178}


## Notas adicionales

## Referencias
