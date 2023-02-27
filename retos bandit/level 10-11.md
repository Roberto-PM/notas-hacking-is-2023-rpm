# LEVEL 10-11

## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

## Datos acceso
ssh bandit# @bandit.labs.overthewire.org -p 2220
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

## Solucion
```bash
bandit10@bandit:~$ ls
data.txt 
bandit10@bandit:~$ cat data.txt VGhlIHBhc3N3b3JkIGlzIElGdWt3S0dzRlc4TU9xM0lSRnFyeEUxaHhUTkViVVBSCg== 
bandit10@bandit:~$ bandit10@bandit:~$ echo "hola mundo" 
hola mundo 
bandit10@bandit:~$ echo "hola mundo" | base64 
aG9sYSBtdW5kbwo= 
bandit10@bandit:~$ echo -n aG9sYSBtdW5kbwo= | base64 -d 
hola mundo bandit10@bandit:~$ base64 -d data.txt 
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM 
bandit10@bandit:~$ 
bandit10@bandit:~$ cat data.txt VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg== 
bandit10@bandit:~$ cat data.txt | base64 -d 
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```

## Notas adicionales
Base 64: Para codificar o decodificar la entrada/salida estándar o cualquier contenido de archivo, Linux utiliza el sistema de codificación y decodificación base64. Los datos se codifican y decodifican para facilitar el proceso de transmisión y almacenamiento de datos. La codificación y la decodificación no son similares al cifrado y descifrado. Los datos codificados se pueden revelar fácilmente mediante la decodificación. Por lo tanto, esta herramienta de utilidad de línea de comandos no se puede utilizar para la seguridad de los datos. El alfabeto, el número y el símbolo '=' se utilizan para codificar cualquier dato.
Sintaxis:
base64 [OPCIÓN] [INFILE] [OUTFILE]
Puede usar diferentes tipos de opciones con el comando base64. Los datos se pueden tomar de cualquier archivo o entrada estándar durante la codificación o decodificación. Después de codificar o decodificar, puede enviar la salida en un archivo o imprimir la salida en el terminal.
**-e o –encode**
This option is used to encode any data from standard input or from any file. It is the default option.
**-d o –decode**  
This option is used to decode any encoded data from standard input or from any file.
## Referencias
https://linuxhint.com/bash_base64_encode_decode/