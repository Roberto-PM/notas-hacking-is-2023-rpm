# pw crack 3


## Descripcion
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/25/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/25/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/25/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Pistas
To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bin`
To exit `bvi` type `:q` and press enter.
The `str_xor` function does not need to be reverse engineered for this challenge.

## Solucion
```bash
roberto-pm-picoctf@webshell:~$ ls
level3.flag.txt.enc  level3.hash.bin  level3.py
roberto-pm-picoctf@webshell:~$ bvi level3.hash.bin 

bvi version 1.4.0 Copyright (C) 1996-2014 by Gerhard Buergmann
roberto-pm-picoctf@webshell:~$ nano level3.py
roberto-pm-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: 8799
That password is incorrect
roberto-pm-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: d3ab
That password is incorrect
roberto-pm-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: 1ea2
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}
roberto-pm-picoctf@webshell:~$ 
```
al ejecutar nano podemos leer el codigo que verifica la contrasena contiene esto:
pos_pw_list = ["8799", "d3ab", "1ea2", "acaf", "2295", "a9de", "6f3d"]
probando una por una da como resultado que la correcta es 1ea2

## Bandera
picoCTF{m45h_fl1ng1ng_6f98a49f}
## Notas adicionales


## Referencias
