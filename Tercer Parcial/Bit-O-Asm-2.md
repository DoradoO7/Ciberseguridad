

## Descripcion
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt).
## Pistas
- `PTR`'s or 'pointers', reference a location in memory where values can be stored.
## Solucion
```
Es muy parecido al bit o asm1 y veremos que hacia eax es el de la direccion rbp-0x4 por lo que vemos que en la anterior instruccion se le dio el valor de 0x9fe1a por lo que ese es el valor de eax convirtiendolo a decimalsu numero es 654874 el cual es el de la flag
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0x4],0x9fe1a
<+22>:    mov    eax,DWORD PTR [rbp-0x4]
<+25>:    pop    rbp
<+26>:    ret

```

## Bandera

picoCTF{654874}

## Notas adicionales

## Referencias
- [HEXtoDEC](https://www.rapidtables.com/convert/number/hex-to-decimal.html)