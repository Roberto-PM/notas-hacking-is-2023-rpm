# LEVEL 11-12

## Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Datos acceso
ssh bandit11 @bandit.labs.overthewire.org -p 2220
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

## Solucion
```bash
bandit11@bandit:~$ ls 
data.txt 
bandit11@bandit:~$ cat data.txt 
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi 
bandit11@bandit:~$ cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M] 
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv bandit11@bandit:~$
```
## Notas adicionales
tr is a **command-line utility** in Linux and Unix systems that translates, deletes, and squeezes characters from the standard input and writes the result to the standard output. The tr command can perform operations like removing repeated characters, converting uppercase to lowercase, and basic character replacing and removing.

## Referencias
[Tr Command in Linux with Examples | Linuxize](https://linuxize.com/post/linux-tr-command/#:~:text=tr%20is%20a%20command-line%20utility%20in%20Linux%20and,to%20lowercase%2C%20and%20basic%20character%20replacing%20and%20removing.)


