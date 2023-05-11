
## Objetivos
The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://jupiter.challenges.picoctf.org/static/cd51b2c95be9f3626db6fe6665afb5a3/need-for-speed).

## Solucion
usaremos el comando de readelf -S e igualmente la version de -x
tambien el objdumb 
└─$ objdump -t need-for-speed 
veremos todas las funciones que tiene
usaremos gdb para la solucion de este problema
linea en 938 con control-T pondremos 5 90
PICOCTF{Good job keeping bus #24c43740 speeding along!}

## Referencias
[ELF](https://www.ibm.com/docs/en/ztpf/1.1.0.15?topic=linkage-executable-linking-format-elf)
[x64](https://www.intel.com/content/dam/develop/external/us/en/documents/introduction-to-x64-assembly-181178.pdf)
