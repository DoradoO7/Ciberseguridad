# Level 16 al 17
## Objetivos
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
## datos de acceso
bandit16
JQttfApK4SeyHwDlI9SXGR50qclOAil1
## Solucion
```bash
bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 21 22:02:58 2023 GMT; NotAfter: Feb 21 22:03:58 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIELZxFNDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjIxMjIwMjU4WhcNMjMwMjIxMjIwMzU4WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC8
C8jJ2//6TxiFBwjuC7+xUcu293V+n8pLxHfVnpZG9fvlOBG3nA3hm2/iNYybZNla
R58hZmfPWEKcuX7GZGvNUOAa6wOg2WYrMo1+6NCcynmCdJEabv2kemvOtBQFeV43
EUW+BW/+6903QuSHsjDewSoljGtmRGjg0oXUgyOlzGDQR/EfX7N8KGubYzZcHf+i
C:\Users\dorad\Desktop>ssh -i llave.txt
usage: ssh [-46AaCfGgKkMNnqsTtVvXxYy] [-B bind_interface]
           [-b bind_address] [-c cipher_spec] [-D [bind_address:]port]
           [-E log_file] [-e escape_char] [-F configfile] [-I pkcs11]
           [-i identity_file] [-J [user@]host[:port]] [-L address]
           [-l login_name] [-m mac_spec] [-O ctl_cmd] [-o option] [-p port]
           [-Q query_option] [-R address] [-S ctl_path] [-W host:port]
           [-w local_tun[:remote_tun]] destination [command]

C:\Users\dorad\Desktop>ssh -i llave.txt bandit17@bandit.labs.overthewire.org -p2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|



bandit17@bandit:~$ cat /etc/
Display all 215 possibilities? (y or n)
bandit17@bandit:~$ cat /etc/bandit_pass//bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
bandit17@bandit:~$

```
## Notas adicionales
nmap localhost pruba los primeros 1000 puertos
Netcat ayuada para tener un host abierto
## Referencias

[Port scanner on Wikipedia](https://en.wikipedia.org/wiki/Port_scanner)
