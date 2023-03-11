# Firt Grep


## Descripcion

## Pistas
usar comando grep

## Solucion
```bash
roberto-pm-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/515f19f3612bfd97cd3f0c0ba32bd864/file
--2023-03-05 23:34:58--  https://jupiter.challenges.picoctf.org/static/515f19f3612bfd97cd3f0c0ba32bd864/file
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 14551 (14K) [application/octet-stream]
Saving to: 'file'

file                                           100%[=================================================================================================>]  14.21K  --.-KB/s    in 0s      

2023-03-05 23:34:58 (181 MB/s) - 'file' saved [14551/14551]

roberto-pm-picoctf@webshell:~$ ls
README.txt  file  strings

roberto-pm-picoctf@webshell:~$ egrep 'pico' file
picoCTF{grep_is_good_to_find_things_5af9d829}
```

## Bandera
picoCTF{grep_is_good_to_find_things_5af9d829}
## Notas adicionales


## Referencias
