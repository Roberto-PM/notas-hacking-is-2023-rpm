# LEVEL 1-2

## Objetivo
The password for the next level is stored in a file called **-** located in the home directory

## Datos acceso
ssh bandit1@bandit.labs.overthewire.org -p 2220
bandit1
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
## Solucion
```bash
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat -
^C
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$
```

## Notas adicionales
abrir archivos con "-"
This type of approach has a lot of misunderstanding because using **-** as an argument refers to **STDIN/STDOUT** i.e **dev/stdin** or **dev/stdout** .So if you want to open this type of file you have to specify the full location of the file such as **./-** .For eg. , 
if you want to see what is in that file use **cat ./-**

## Referencias
[linux - How to open a "-" dashed filename using terminal? - Stack Overflow](https://stackoverflow.com/questions/42187323/how-to-open-a-dashed-filename-using-terminal)