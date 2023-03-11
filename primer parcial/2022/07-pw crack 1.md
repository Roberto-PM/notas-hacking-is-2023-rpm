# pw crack 1


## Descripcion
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/53/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/53/level1.flag.txt.enc) in the same directory too.
## Pistas
To view the file in the webshell, do: `$ nano level1.py`
To exit `nano`, press Ctrl and x and follow the on-screen prompts.
The `str_xor` function does not need to be reverse engineered for this challenge.

## Solucion
```bash
roberto-pm-picoctf@webshell:~$ ls
README.txt  fixme1.py  fixme2.py  level1.flag.txt.enc  level1.py
roberto-pm-picoctf@webshell:~$ nano level1.py
roberto-pm-picoctf@webshell:~$ python3 level1.py
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}
roberto-pm-picoctf@webshell:~$ 
```
al ejecutar nano podemos leer el codigo que verifica la contrasena que es 8713
## Bandera
picoCTF{545h_r1ng1ng_1b2fd683}
## Notas adicionales


## Referencias
