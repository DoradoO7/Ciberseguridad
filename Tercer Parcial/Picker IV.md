

## Descripcion
Can you figure out how this program works to get the flag?Connect to the program with netcat:`$ nc saturn.picoctf.net 53060`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/527/picker-IV.c). The binary can be downloaded [here](https://artifacts.picoctf.net/c/527/picker-IV).
## Pistas
- With Python, there are no binaries. With compiled languages like C, there is source code, and there are binaries. Binaries are created from source code, they are a conversion from the human-readable source code, to the highly efficient machine language, in this case: x86_64.
- How can you find the address that `win` is at?
## Solucion
```
Descargamos el archivo y analizamos el codigo ensamblador con gdb y el comando layout asm despues buscaremos donde dega win 
la direccion donde inicia win es 0x40129e por lo que la ingresamos
nos metemos al nc que se nos da y colocamos la direcion de win
Enter the address in hex to jump to, excluding '0x': 40129e
You input 0x40129e
You won!
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_14bc5444}
```

## Bandera

picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_14bc5444}

## Notas adicionales

## Referencias
