# LEVEL 27-28

## Objetivo
There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

## Datos acceso
ssh bandit27 @bandit.labs.overthewire.org -p 2220
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
## Solucion
```bash
bandit27@bandit:~$ mktemp -d
/tmp/tmp.pR0V3f1er0
bandit27@bandit:~$ cd /tmp/tmp.pR0V3f1er0
bandit27@bandit:/tmp/tmp.pR0V3f1er0$  git clone ssh://bandit27-git@localhost/home/bandit27-git/repo
Cloning into 'repo'...
The authenticity of host 'localhost (127.0.0.1)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit27/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit27/.ssh/known_hosts).

                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

!!! You are trying to log into this SSH server on port 22, which is not intended.

bandit27-git@localhost: Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
bandit27@bandit:/tmp/tmp.pR0V3f1er0$ git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
Cloning into 'repo'...
kex_exchange_identification: read: Connection reset by peer
Connection reset by 127.0.0.1 port 2220
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
bandit27@bandit:/tmp/tmp.pR0V3f1er0$  git clone ssh://bandit27-
Cloning into 'bandit27-'...
localhofatal: no path specified; see 'git help pull' for valid url syntaxst:2220
bandit27@bandit:/tmp/tmp.pR0V3f1er0$ git@localhost:2220/home/bandit27-git/repo
-bash: git@localhost:2220/home/bandit27-git/repo: No such file or directory
bandit27@bandit:/tmp/tmp.pR0V3f1er0$ git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit27/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit27/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit27-git@localhost's password:
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
bandit27@bandit:/tmp/tmp.pR0V3f1er0$ ls
repo
bandit27@bandit:/tmp/tmp.pR0V3f1er0$ cd repo
bandit27@bandit:/tmp/tmp.pR0V3f1er0/repo$ ls
README
bandit27@bandit:/tmp/tmp.pR0V3f1er0/repo$ cat README
The password to the next level is: AVanL161y9rsbcJIsFHuw35rjaOM19nR
bandit27@bandit:/tmp/tmp.pR0V3f1er0/repo$
```
## Notas adicionales

## Referencias

c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1