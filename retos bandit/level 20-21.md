# LEVEL 20-21

## Objetivo
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

## Datos acceso
ssh bandit20 @bandit.labs.overthewire.org -p 2220
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
## Solucion
```bash
bandit20@bandit:~$ nc -lnvp 2020 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[1] 1003596
bandit20@bandit:~$ Listening on 0.0.0.0 2020

bandit20@bandit:~$  ./suconnect 2020
Connection received on 127.0.0.1 58764
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
[1]+  Done                    nc -lnvp 2020 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit20@bandit:~$
```
## Notas adicionales
nc -lnvp 2020 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
Este comando es utilizado para crear un socket de red usando Netcat, un programa utilizado para leer y escribir datos a través de conexiones de red utilizando protocolos TCP o UDP. Aquí está una explicación detallada de cada parte del comando:

-   "nc": este es el comando que inicia la aplicación Netcat.
-   "-l": esta opción indica que Netcat debe estar en modo "escucha" para esperar una conexión entrante.
-   "-n": esta opción indica que Netcat no debe resolver nombres de host o números de puerto, y debe mostrar las direcciones IP y los números de puerto sin resolución inversa.
-   "-v": esta opción activa el modo detallado, lo que significa que se mostrará información adicional durante la ejecución del comando.
-   "-p 2020": esta opción indica que Netcat debe usar el puerto 2020 para la conexión entrante.
-   "<<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT": esta es la entrada de datos del comando, que se transmite a Netcat a través de la red como si fuera una conexión entrante. En este caso, la entrada de datos es una cadena de texto "VxCazJaVykI6W36BkBU0mJTCM8rR95XT".
-   "&": este símbolo se utiliza para poner el comando en segundo plano, lo que significa que se ejecutará en segundo plano mientras se puede utilizar la terminal para ejecutar otros comandos.

En resumen, este comando inicia Netcat en modo de escucha en el puerto 2020 para esperar una conexión entrante. Cuando se establece una conexión, cualquier entrada de datos enviada a través de la conexión se transmite como una cadena de texto "VxCazJaVykI6W36BkBU0mJTCM8rR95XT". Además, el comando se ejecuta en segundo plano debido al uso del símbolo "&".

El comando "./suconnect 2020" se utiliza para conectarse a la instancia de Netcat en modo de escucha en el puerto 2020, que fue creada previamente con el comando "nc -lnvp 2020 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &".
## Referencias

https://www.ionos.mx/digitalguide/servidores/herramientas/netcat/