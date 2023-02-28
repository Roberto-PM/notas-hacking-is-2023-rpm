# LEVEL 17-18

## Objetivo
There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

## Datos acceso
ssh bandit17 @bandit.labs.overthewire.org -p 2220
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
## Solucion
```bash
bandit17@bandit:~$ ls -la
total 36
drwxr-xr-x  3 root     root     4096 Feb 21 22:02 .
drwxr-xr-x 70 root     root     4096 Feb 21 22:04 ..
-rw-r-----  1 bandit17 bandit17   33 Feb 21 22:02 .bandit16.password
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit18 bandit17 3300 Feb 21 22:02 passwords.new
-rw-r-----  1 bandit18 bandit17 3300 Feb 21 22:02 passwords.old
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
drwxr-xr-x  2 root     root     4096 Feb 21 22:02 .ssh
bandit17@bandit:~$  diff passwords.old passwords.new --color
42c42
< f9wS9ZUDvZoo3PooHgYuuWdawDFvGld2
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
bandit17@bandit:~$
```

## Notas adicionales
Específicamente, el comando "diff" compara los contenidos de los dos archivos línea por línea y muestra las líneas que son diferentes. Para las líneas que son diferentes, "diff" muestra el contenido de ambas líneas y resalta las diferencias utilizando códigos de color  al colocar la opcion --color. Por ejemplo, las líneas que se han agregado a "passwords.new" pueden aparecer en verde, mientras que las líneas que se han eliminado de "passwords.old" pueden aparecer en rojo.
## Referencias
https://geekland.eu/comparar-directorios-y-archivos-comando-diff-linux/#:~:text=diff%3A%20Es%20la%20utilidad%20para,están%20dentro%20del%20directorio%20analizado.