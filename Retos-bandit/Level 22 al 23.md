# Level 22 al 23
## Objetivos

A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.
**NOTE:** Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

## datos de acceso
bandit22
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
## Solucion

```bash
bandit22@bandit:~$ ls /etc/cr
cron.d/               cron.hourly/          crontab               cryptsetup-initramfs/
cron.daily/           cron.monthly/         cron.weekly/          crypttab
bandit22@bandit:~$ ls /etc/cron.d -la
total 56
drwxr-xr-x   2 root root  4096 Feb 21 22:04 .
drwxr-xr-x 108 root root 12288 Feb 21 22:04 ..
-rw-r--r--   1 root root    62 Feb 21 22:02 cronjob_bandit15_root
-rw-r--r--   1 root root    62 Feb 21 22:02 cronjob_bandit17_root
-rw-r--r--   1 root root   120 Feb 21 22:03 cronjob_bandit22
-rw-r--r--   1 root root   122 Feb 21 22:03 cronjob_bandit23
-rw-r--r--   1 root root   120 Feb 21 22:03 cronjob_bandit24
-rw-r--r--   1 root root    62 Feb 21 22:03 cronjob_bandit25_root
-rw-r--r--   1 root root   201 Jan  8  2022 e2scrub_all
-rwx------   1 root root    52 Feb 21 22:04 otw-tmp-dir
-rw-r--r--   1 root root   102 Mar 23  2022 .placeholder
-rw-r--r--   1 root root   396 Feb  2  2021 sysstat
bandit22@bandit:~$ ls /etc/cron.d/cronjob_bandit23
/etc/cron.d/cronjob_bandit23
bandit22@bandit:~$ cat  /etc/cron.d/cronjob_bandit23
@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
bandit22@bandit:~$ cat /usr/bin/cronjob_bandit_bandit23.sh
cat: /usr/bin/cronjob_bandit_bandit23.sh: No such file or directory
bandit22@bandit:~$ cat /usr/bin/cronjob_bandit23.sh
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget
bandit22@bandit:~$ whoami
bandit22
bandit22@bandit:~$ myname=$(whoami)
bandit22@bandit:~$ echo $myname
bandit22
bandit22@bandit:~$ echo I am user $myname | md5sum
8169b67bd894ddbb4412f91573b38db3  -
bandit22@bandit:~$ echo I am user $myname | md5sum | cut -d ' ' -f 1
8169b67bd894ddbb4412f91573b38db3
bandit22@bandit:~$ myname=bandit23
bandit22@bandit:~$ echo I am user $myname | md5sum | cut -d ' ' -f 1
8ca319486bfbbc3663ea0fbe81326349
bandit22@bandit:~$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
bandit22@bandit:~$
```
## Notas adicionales

## Referencias



