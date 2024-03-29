# Bandit Level 28 → Level 29
## Objetivo
There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

Clone the repository and find the password for the next level.

## Datos de acceso al nivel
bandit28
AVanL161y9rsbcJIsFHuw35rjaOM19nR
## Solucion
```
bandit28@bandit:/$ mkdir /tmp/Dorado
bandit28@bandit:/$ cd /tmp/Dorado
bandit28@bandit:/tmp/Dorado$ git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
Cloning into 'repo'...
bandit28-git@localhost's password: 
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 9 (delta 2), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (9/9), 799 bytes | 159.00 KiB/s, done.
Resolving deltas: 100% (2/2), done.
bandit28@bandit:/tmp/Dorado$ cd repo
bandit28@bandit:/tmp/Dorado/repo$ ls
README.md
bandit28@bandit:/tmp/Dorado/repo$ cat README.md 
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx

bandit28@bandit:/tmp/Dorado/repo$ git log
commit 104db85a904e9691ff22aafe1a96124c88f75afa (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    fix info leak

commit 6c3c5e485cc531e5d52c321587ce1103833ab7c3
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    add missing data

commit cd3b97ef95879ec34df0d6c82f2a96d552f0e56c
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    initial commit of README.md
bandit28@bandit:/tmp/Dorado/repo$ git checkout 6c3c5e485cc531e5d52c321587ce1103833ab7c3
Note: switching to '6c3c5e485cc531e5d52c321587ce1103833ab7c3'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 6c3c5e4 add missing data
bandit28@bandit:/tmp/Dorado/repo$ cat README.md 
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S


```
## Notas adicionales
_git clone_ es una utilidad de línea de comandos de Git que se utiliza para fijar como objetivo un repositorio y crear una copia de él.
## Referencias
- [thanoskourt OvertheWire](https://thanoskoutr.com/posts/ctfs/overthewire/bandit/levels-20-29/)