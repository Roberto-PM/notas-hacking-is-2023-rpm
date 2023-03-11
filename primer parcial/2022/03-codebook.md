# Codebook


## Descripcion
Run the Python script `code.py` in the same directory as `codebook.txt`.

-   [Download code.py](https://artifacts.picoctf.net/c/100/code.py)
-   [Download codebook.txt](https://artifacts.picoctf.net/c/100/codebook.txt)
## Pistas
On the webshell, use `ls` to see if both files are in the directory you are in
The `str_xor` function does not need to be reverse engineered for this challenge.

## Solucion
```bash
roberto-pm-picoctf@webshell:~$ ls
Addadshashanammu  Addadshashanammu.zip  README.txt  code.py  codebook.txt  convertme.py  runme.py
roberto-pm-picoctf@webshell:~$ python3 code.py
picoCTF{c0d3b00k_455157_d9aa2df2}
roberto-pm-picoctf@webshell:~$ 

```
## Bandera
picoCTF{c0d3b00k_455157_d9aa2df2}
## Notas adicionales


## Referencias
