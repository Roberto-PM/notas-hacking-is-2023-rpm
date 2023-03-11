# Strings it


## Descripcion
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings) without running it?
## Pistas


## Solucion
```bash
roberto-pm-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings
--2023-03-02 19:05:17--  https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: 'strings.1'

strings.1                                     100%[=================================================================================================>] 757.84K  1.85MB/s    in 0.4s    

2023-03-02 19:05:18 (1.85 MB/s) - 'strings.1' saved [776032/776032]

roberto-pm-picoctf@webshell:~$ ls      
README.txt  strings  strings.1
roberto-pm-picoctf@webshell:~$ strings strings | grep pico
picoCTF{5tRIng5_1T_7f766a23}
roberto-pm-picoctf@webshell:~$ 
```
## Bandera
picoCTF{5tRIng5_1T_7f766a23}
## Notas adicionales


## Referencias
