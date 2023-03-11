# Based


## Descripcion
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29956`.

## Pistas
I hear python can convert things.
It might help to have multiple windows open.

## Solucion
```bash
roberto-pm-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 29956
Let us see how data is stored
socket
Please give the 01110011 01101111 01100011 01101011 01100101 01110100 as a word.
...
you have 45 seconds.....

Input:
socket
Please give me the  163 154 165 144 147 145 as a word.
Input:
sludge
Please give me the 736f636b6574 as a word.
Input:
socket
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_b375bb16}
^C
roberto-pm-picoctf@webshell:~$ 
```

## Bandera
picoCTF{learning_about_converting_values_b375bb16}
## Notas adicionales
con ayuda de cyberchef se logro decifrar rapidamente todos los textos codificados y su tipo
el primero estaba en binario
el segundo en octal
el terceroen hexadecimal

## Referencias
