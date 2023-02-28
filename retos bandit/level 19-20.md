# LEVEL 19-20

## Objetivo
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

## Datos acceso
ssh bandit19 @bandit.labs.overthewire.org -p 2220
awhqfNnAbc1naukrpqDYcF95h7HoMTrC

## Solucion
```bash
bandit19@bandit:~$ ls
bandit20-do
bandit19@bandit:~$ ./bandit20-do
Run a command as another user.
  Example: ./bandit20-do id
bandit19@bandit:~$ whoami
bandit19
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit19@bandit:~$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Feb 21 22:03 .
drwxr-xr-x 70 root     root      4096 Feb 21 22:04 ..
-rwsr-x---  1 bandit20 bandit19 14876 Feb 21 22:03 bandit20-do
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
bandit19@bandit:~$
```

## Notas adicionales
en linux existe la posibilidad de correr comandos como otro usuario
Los permisos "-rwsr-x---" indican los permisos de acceso para un archivo en un sistema operativo Unix o Unix-like. Aquí está una explicación detallada de cada caracter:
-   El primer carácter "-" indica que se trata de un archivo regular. Si fuera un directorio, aparecería "d" en su lugar.
-   Los siguientes tres caracteres "rws" indican los permisos del usuario propietario. "r" indica que el propietario puede leer el archivo, "w" indica que el propietario puede escribir en el archivo, y "s" indica que el archivo se ejecuta con los permisos de su propietario y no del usuario que lo ejecuta.
-   Los siguientes tres caracteres "r-x" indican los permisos del grupo al que pertenece el archivo. "r" indica que los miembros del grupo pueden leer el archivo, "-" indica que no pueden escribir en el archivo, y "x" indica que los miembros del grupo pueden ejecutar el archivo.
-   Los últimos tres caracteres "---" indican los permisos para otros usuarios que no son el propietario ni miembros del grupo. "-" indica que no tienen permiso de lectura, "-" indica que no tienen permiso de escritura, y "-" indica que no tienen permiso de ejecución.
## Referencias

https://www.baeldung.com/linux/run-as-another-user