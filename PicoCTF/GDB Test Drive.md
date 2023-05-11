## Objetivos
Can you get the flag? Download this [binary](https://artifacts.picoctf.net/c/87/gdbme). Here's the test drive instructions:
-   `$ chmod +x gdbme`
-   `$ gdb gdbme`
-   `(gdb) layout asm`
-   `(gdb) break *(main+99)`
-   `(gdb) run`
-   `(gdb) jump *(main+104)`
## Solucion
usaremos nuevamente el gdb solo que ahora correremos el programa y nos saltaremos una call que es la q nos provoca que no jale introduciremos al codigo en asm el (main+99) y despues el jump para q salte la instrucion jump*(main+104)
y al correrlo nos dara la flag 
```
picoCTF{d3bugg3r_dr1v3_7776d758}
````
## Referencias
[ayuda](https://github.com/arvindshima/PicoCTF-2022/blob/main/Reverse%20Engineering/gdb-test-drive.md)

