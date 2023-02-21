# Level 14 al 15

## Objetivos
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.
## datos de acceso
bandit14 
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

## Solucion
```bash
bandit14@bandit:~$ nc localhost 3000
bandit14@bandit:~$ nc localhost 30000
^C
bandit14@bandit:~$ nc localhost 30000

Wrong! Please enter the correct current password

bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

^C
bandit14@bandit:~$
```
## Notas adicionales

## Referencias

-   [How the Internet works in 5 minutes (YouTube)](https://www.youtube.com/watch?v=7_LPdttKXPc) 
-   [IP Addresses](http://computer.howstuffworks.com/web-server5.htm)
-   [IP Address on Wikipedia](https://en.wikipedia.org/wiki/IP_address)
-   [Localhost on Wikipedia](https://en.wikipedia.org/wiki/Localhost)
-   [Ports](http://computer.howstuffworks.com/web-server8.htm)
-   [Port (computer networking) on](https://en.wikipedia.org/wiki/Port_(computer_networking))
