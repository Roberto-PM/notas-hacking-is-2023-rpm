# LEVEL 2-3

## Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory

## Datos acceso
ssh bandit2@bandit.labs.overthewire.org -p 2220
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

## Solucion
```bash
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$
```
## Notas adicionales
los archivos con espacios en su nombre se pueden acceder agregando barras diagonales ates de cada espacio o encerrandolos entre comillas
## Referencias

