# LEVEL 8-9

## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

## Datos acceso
ssh bandit8 @bandit.labs.overthewire.org -p 2220
TESKZC0XvTetK0S9xNwm25STk5iWrBvP

## Solucion
```bash
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ wc data.txt
 1001  1001 33033 data.txt
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$
```

## Notas adicionales
sort ordena todo el contenido de un archivo
uniq muestra las lineas que solo existen una vez

## Referencias

