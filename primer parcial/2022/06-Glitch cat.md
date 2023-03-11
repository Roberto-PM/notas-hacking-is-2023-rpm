# Glitch cat


## Descripcion
Our flag printing service has started glitching!`$ nc saturn.picoctf.net 65353`
## Pistas
ASCII is one of the most common encodings used in programming
We know that the glitch output is valid Python, somehow!
Press Ctrl and c on your keyboard to close your connection and return to the command prompt.

## Solucion
```bash
roberto-pm-picoctf@webshell:~$ 
roberto-pm-picoctf@webshell:~$ nc saturn.picoctf.net 65353
'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
```
leyendo el codigo se busca un conversor de ascii a texto para cada chc()
https://photo333.com/ascii-to-text-es.php

## Bandera
picoCTF{gl17ch_m3_n07_9c42a45d}
## Notas adicionales
-   `chr(0x39)`: Este es un carácter especial que no es visible en la cadena, pero representa el carácter con el código ASCII 0x39, que es el número 9.
-   `chr(0x63)`: Este es otro carácter especial que representa el código ASCII 0x63, que es la letra minúscula c.
-   `chr(0x34)`: Esto representa el código ASCII 0x34, que es el número 4.
-   `chr(0x32)`: Esto representa el código ASCII 0x32, que es el número 2.
-   `chr(0x61)`: Esto representa el código ASCII 0x61, que es la letra minúscula a.
-   `chr(0x34)`: Esto representa el código ASCII 0x34, que es el número 4.
-   `chr(0x35)`: Esto representa el código ASCII 0x35, que es el número 5.
-   `chr(0x64)`: Esto representa el código ASCII 0x64, que es la letra minúscula d.

## Referencias
