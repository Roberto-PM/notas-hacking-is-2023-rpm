# LEVEL 31-32

## Objetivo
There is a git repository at `ssh://bandit31-git@localhost:2220/home/bandit31-git/repo`. The password for the user `bandit31-git` is the same as for the user `bandit31`.

Clone the repository and find the password for the next level.

## Datos acceso
ssh bandit31 @bandit.labs.overthewire.org -p 2220
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
## Solucion
```bash
bandit31@bandit:/tmp/tmp.Bu1cHjphlg$ ls
repo
bandit31@bandit:/tmp/tmp.Bu1cHjphlg$ cd repo
bandit31@bandit:/tmp/tmp.Bu1cHjphlg/repo$ ls
README.md
bandit31@bandit:/tmp/tmp.Bu1cHjphlg/repo$ cat README.md
This time your task is to push a file to the remote repository.

Details:
    File name: key.txt
    Content: 'May I come in?'
    Branch: master

bandit31@bandit:/tmp/tmp.Bu1cHjphlg/repo$ echo May I come in? > key.txt
bandit31@bandit:/tmp/tmp.Bu1cHjphlg/repo$ cat key.txt
May I come in?
bandit31@bandit:/tmp/tmp.Bu1cHjphlg/repo$ git add -f key.txt
bandit31@bandit:/tmp/tmp.Bu1cHjphlg/repo$ git commit -a
Unable to create directory /home/bandit31/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

Unable to create directory /home/bandit31/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

[master a718197] llave
 1 file changed, 1 insertion(+)
 create mode 100644 key.txt
bandit31@bandit:/tmp/tmp.Bu1cHjphlg/repo$ git push origin master
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password:
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 319 bytes | 319.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: ### Attempting to validate files... ####
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
remote: Well done! Here is the password for the next level:
remote: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
To ssh://localhost:2220/home/bandit31-git/repo
 ! [remote rejected] master -> master (pre-receive hook declined)
error: failed to push some refs to 'ssh://localhost:2220/home/bandit31-git/repo'
bandit31@bandit:/tmp/tmp.Bu1cHjphlg/repo$
```
## Notas adicionales
El comando "git add -f" se utiliza en Git para forzar la adición de archivos al área de preparación (staging area), incluso si los archivos están ignorados por Git o si se ha establecido un patrón de exclusión (como en el archivo .gitignore).

El comando "git commit -a" se utiliza en Git para agregar y confirmar cambios en todos los archivos modificados o eliminados en el directorio de trabajo (working directory), sin necesidad de usar el comando "git add" previamente.

La opción "-a" significa "all" (todos) y le indica a Git que debe agregar y confirmar los cambios en todos los archivos que se hayan modificado o eliminado desde el último commit, sin tener que pasar por el proceso de agregar los archivos al área de preparación (staging area).
## Referencias

