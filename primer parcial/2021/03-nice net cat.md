# Nice net cat


## Descripcion
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 35652`, but it doesn't speak English...
## Pistas
You can practice using netcat with this picoGym problem: [what's a netcat](https://play.picoctf.org/practice/challenge/34)
You can practice reading and writing ASCII with this picoGym problem: [Let's Warm Up](https://play.picoctf.org/practice/challenge/22)

## Solucion
```bash
roberto-pm-picoctf@webshell:~$ nc mercury.picoctf.net 35652 | awk '{printf("%c",$1)}'
picoCTF{g00d_k1tty!_n1c3_k1tty!_9b3b7392}
```
## Bandera
picoCTF{g00d_k1tty!_n1c3_k1tty!_9b3b7392}
## Notas adicionales
Este comando de `awk` en Linux toma el contenido de la entrada estándar (STDIN) y muestra el primer campo (columna) de cada línea, interpretándolo como un valor ASCII que representa un carácter, y lo imprime en la salida estándar (STDOUT).

Más específicamente, el comando utiliza el comando `printf` de awk para imprimir el valor ASCII del primer campo de cada línea. El formato utilizado en `printf` es `%c`, que especifica que el argumento siguiente debe ser interpretado como un carácter ASCII.

Entonces, el resultado final es que el comando imprime en la pantalla una cadena de caracteres que representan los valores ASCII del primer campo de cada línea de entrada.

## Referencias
