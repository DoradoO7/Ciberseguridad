## Objetivos
Connect to this PostgreSQL server and find the flag!
Additional details will be available after launching your challenge instance.
## Solucion
Observaremos que lso msj estan encriptados y encontramos uno que no lo esta y le damos un clik como http stream
filtros: tcp.stream eq 5 le damos click a los archivos siguiendolos
como http hasta que vemos  en uno cvpbPGS{c33xno00_1_ lo que posiblemente sea la bandera codificada
usaremos cyberchef con ret13 
obteniendo la bandera picoCTF{p33kab00_1_s33_u_deadbeef}

## Referencias
[ayuda de gamplay](https://www.youtube.com/watch?v=0Btqp9ew9dE)