
## Descripcion
This program has constructed the flag using hex ascii values. Identify the flag text by disassembling the program.You can download the file from [here](https://artifacts.picoctf.net/c/506/asciiftw).
## Pistas
- The combined range of hex-ascii for English alphabets and numerical digits is from 30 to 7A.
- Online hex-ascii converters can be helpful.
## Solucion
```
Descargamos el archivo y con la herramienta de gdb desensamblamos el main 
gdb dissamble main 
la pista indicaba que iniciaba por 70 por lo que seguimos tomando los primeros valores y convirtiendolos a ascii asi obteniendo la bandera:
70 69 63 6f 43 54 46 7b 41 53 43 49 49 5f 49 53 5f 45 41 53 59 5f 37 42 43 44 39 37 31 44 7d eso seria 
picoCTF{ASCII_IS_EASY_7BCD971D}
```

## Bandera

picoCTF{ASCII_IS_EASY_7BCD971D}

## Notas adicionales

## Referencias
- [HEXtoASCII](https://www.rapidtables.com/convert/number/hex-to-ascii.html)