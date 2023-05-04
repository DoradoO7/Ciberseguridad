## Objetivos
What does asm1(0x6fa) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/b41e08fc19ceb9d0466ebd68d36c5630/test.S)
## Solucion
Descargamos y analizamos el archivo con el valor que nos dieron 0x3a2 que por lo general indica el main:
Empieza el codigo en la linea 0 iniciandolo con el push ebp despues se pasa a la linea 1 pasandole el valor de esp a ebp despues en la linea 3 se hace una comparacion en la que compara si la afirmacion es correcta por lo que se mueve a la linea 37 del codigo observamos que se trata de una comparacion del tipo que salta si son diferentes los valores son iguales por lo que no se realiza el salto y nos movemos a la linea 46 del codigo donde se mueve el valor de inicial a eax despues en la linea 49 a eax se le resta obteniendo un nuevo valor continua a la linea 52 donde hay un salto a la linea 60 donde hay un pop ebp y despues continua a la 61 donde nos da un retorno al main.

Por lo tanto la bandera es 0x6e8.

## Referencias
[Video de solucion](https://www.youtube.com/watch?v=Dy-gHlymkdo&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=53)