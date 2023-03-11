# LEVEL 32-33

## Objetivo
After all this `git` stuff its time for another escape. Good luck!

## Datos acceso
ssh bandit32 @bandit.labs.overthewire.org -p 2220
rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
## Solucion
```bash
WELCOME TO THE UPPERCASE SHELL
>> a
sh: 1: A: not found
>> ls
sh: 1: LS: not found
>> $0
$ ls
uppershell
$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Feb 21 22:03 .
drwxr-xr-x 70 root     root      4096 Feb 21 22:04 ..
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
-rwsr-x---  1 bandit33 bandit32 15128 Feb 21 22:03 uppershell
$ whoami
bandit33
$ cat /etc/bandit_pass/bandit33
odHo63fHiFqcWWJG9rLiLDtPm45KzUKy
```
## Notas adicionales
En una terminal Bash, el comando "$0" se utiliza para hacer referencia al nombre del shell que se está ejecutando actualmente en la terminal. Este comando es una variable de shell especial que devuelve el nombre del archivo ejecutable que se está utilizando como shell en la sesión de la terminal.
## Referencias

