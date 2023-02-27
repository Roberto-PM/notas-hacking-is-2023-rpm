# LEVEL 9-10

## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.


## Datos acceso
ssh bandit9 @bandit.labs.overthewire.org -p 2220
EN632PlfYiZbn3PhVK3XOGSlNInNE00t

## Solucion
```bash
bandit9@bandit:~$ ls 
data.txt 
bandit9@bandit:~$ 
file data.txt data.txt: data 
bandit9@bandit:~$ strings data.txt | grep == 
c========== the 
h;========== password 
========== isT 
n.E========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s 
bandit9@bandit:~$
```

## Notas adicionales
## QUE USOS PODEMOS DAR AL COMANDO GREP

El comando grep nos permite buscar cadenas de texto y palabras dentro de un fichero de texto o de la entrada estándar de la terminal. Una vez encontrado el contenido que estamos buscando:

1.  grep mostrará en pantalla la totalidad de la línea/s que contiene/n la cadena de texto o palabra que estamos buscando.
2.  Con la opción pertinente únicamente mostrará la cadena de texto o palabra de cada una de las líneas que coincide con nuestro criterio de búsqueda.

## Referencias
https://geekland.eu/uso-del-comando-grep-en-linux-y-unix-con-ejemplos/

