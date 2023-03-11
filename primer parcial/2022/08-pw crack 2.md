# pw crack 8


## Descripcion
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/16/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level2.flag.txt.enc) in the same directory too.
## Pistas
To view the file in the webshell, do: `$ nano level1.py`
To exit `nano`, press Ctrl and x and follow the on-screen prompts.
The `str_xor` function does not need to be reverse engineered for this challenge.

## Solucion
```bash
roberto-pm-picoctf@webshell:~$ ls
level2.flag.txt.enc  level2.py
roberto-pm-picoctf@webshell:~$ nano level2.py
roberto-pm-picoctf@webshell:~$ python3 level2.py 
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
roberto-pm-picoctf@webshell:~$ 
```
al ejecutar nano podemos leer el codigo que verifica la contrasena que es el siguiente
```python
def level_2_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")
```
usando el mismo metodo del glitch cat usando un convertidor acii obtenemos lo siguiente
-   `0x64` representa el carácter `d`
-   `0x65` representa el carácter `e`
-   `0x37` representa el carácter `7`
-   `0x36` representa el carácter `6`

Por lo tanto, la cadena de caracteres `chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36)` se traduce a la cadena de caracteres `de76`.
## Bandera
picoCTF{tr45h_51ng1ng_489dea9a}
## Notas adicionales


## Referencias
