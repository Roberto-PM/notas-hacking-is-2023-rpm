# LEVEL 28-29

## Objetivo
There is a git repository at `ssh://bandit28-git@localhost:2220/home/bandit28-git/repo`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

## Datos acceso
ssh bandit28 @bandit.labs.overthewire.org -p 2220
AVanL161y9rsbcJIsFHuw35rjaOM19nR
## Solucion
```bash
bandit28@bandit:~$ mktemp -d
/tmp/tmp.Udyv7F4zGh
bandit28@bandit:~$ cd /tmp/tmp.Udyv7F4zGh
bandit28@bandit:/tmp/tmp.Udyv7F4zGh$ git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
Cloning into 'repo'...
The authenticity of host [localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit28/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit28/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit28-git@localhosts password:
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 9 (delta 2), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (9/9), 799 bytes | 799.00 KiB/s, done.
Resolving deltas: 100% (2/2), done.

bandit28@bandit:/tmp/tmp.Udyv7F4zGh$ ls
repo
bandit28@bandit:/tmp/tmp.Udyv7F4zGh$ cat repo
cat: repo: Is a directory
bandit28@bandit:/tmp/tmp.Udyv7F4zGh$ cd repo
bandit28@bandit:/tmp/tmp.Udyv7F4zGh/repo$ ls
README.md
bandit28@bandit:/tmp/tmp.Udyv7F4zGh/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx

bandit28@bandit:/tmp/tmp.Udyv7F4zGh/repo$ git log
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
    
bandit28@bandit:/tmp/tmp.Udyv7F4zGh/repo$ git log -p


commit 104db85a904e9691ff22aafe1a96124c88f75afa (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    fix info leak

diff --git a/README.md b/README.md
index b302105..5c6457b 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for level29 of bandit.
 ## credentials

 - username: bandit29
-- password: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
+- password: xxxxxxxxxx


commit 6c3c5e485cc531e5d52c321587ce1103833ab7c3
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    add missing data

diff --git a/README.md b/README.md
index 7ba2d2f..b302105 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for level29 of bandit.
:
```

## Notas adicionales
El comando "git log -p" se utiliza en Git para mostrar el historial de confirmaciones (commits) en un repositorio, junto con los cambios realizados en cada confirmación.

La opción "-p" indica que se desea mostrar los parches (diffs) introducidos por cada confirmación. Esto significa que, en lugar de solo mostrar los mensajes de confirmación, el comando "git log -p" también muestra la diferencia (diff) entre el estado anterior del repositorio y el estado actual introducido por cada confirmación.

Además de mostrar los parches, el comando "git log -p" también puede mostrar información adicional de cada confirmación, como el autor, la fecha y hora de la confirmación, el hash de la confirmación y el mensaje asociado a la confirmación.
## Referencias

c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1