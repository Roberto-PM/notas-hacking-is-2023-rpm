# LEVEL 7-8

## Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**

## Datos acceso
ssh bandit7 @bandit.labs.overthewire.org -p 2220
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

## Solucion
```bash
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ wc data.txt
  98567  197133 4184396 data.txt
bandit7@bandit:~$  grep millionth data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$ cat data.txt | grep millionth
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$
```

## Notas adicionales
The Linux wc command **calculates a file's word, line, character, or byte count**. Far from just being a utility for word processing, wc is a useful tool for a variety of system tasks.
Grep, or global regular expression print, is one of the most versatile and useful Linux commands available. It works by **searching for text and strings that users define in a given file**. In other words, grep enables users to search files for a particular pattern or word and see any lines that contain it
## Referencias

