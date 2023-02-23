# Level 20 al 21
## Objetivos
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).
## datos de acceso
bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
## Solucion
```bash
bandit20@bandit:~$ nc -lnvp 2020
Listening on 0.0.0.0 2020
c
^[^[
^[
^C
bandit20@bandit:~$
bandit20@bandit:~$ nc -lnvp 2020 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[1] 2821279
bandit20@bandit:~$ Listening on 0.0.0.0 2020
./suconnect 2020
Connection received on 127.0.0.1 60012
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
[1]+  Done                    nc -lnvp 2020 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit20@bandit:~$



```
## Notas adicionales
Utilizamos el comando nc -lvp [puerto] seguido de la contraseña que usamos para entrar a el usuario 20 y un & (esto para mandarla a segundo plano y poder hacer lo siguiente)
Despues ponemos el siguiente comando "./suconnect [puerto]"
## Referencias


