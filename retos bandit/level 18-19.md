# LEVEL 18-19

## Objetivo
The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.

## Datos acceso
ssh bandit18 @bandit.labs.overthewire.org -p 2220
hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg

## Solucion
```bash
C:\Users\DELL AL>ssh bandit18@bandit.labs.overthewire.org -p 2220 /bin/bash
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:
ls
readme
cat readme
awhqfNnAbc1naukrpqDYcF95h7HoMTrC
```

## Notas adicionales
Este comando se utiliza para establecer una conexión SSH (Secure Shell) con el servidor de la máquina virtual "bandit.labs.overthewire.org" en el puerto 2220, e iniciar una sesión interactiva de la shell de Bash en el usuario "bandit18".

cada parte del comando:

-   "ssh": este es el comando que se utiliza para establecer una conexión SSH con un servidor remoto.
-   "[bandit18@bandit.labs.overthewire.org](mailto:bandit18@bandit.labs.overthewire.org)": este es el nombre de usuario y el nombre del host del servidor al que se desea conectarse. En este caso, el nombre de usuario es "bandit18" y el nombre del host es "bandit.labs.overthewire.org".
-   "-p 2220": esta opción se utiliza para especificar el puerto que se debe utilizar para la conexión SSH. En este caso, el puerto es 2220.
-   "/bin/bash": esta es la ruta del shell de Bash que se desea iniciar una vez que se establece la conexión SSH. Al especificar "/bin/bash", se inicia una sesión interactiva de la shell de Bash en el usuario "bandit18".
## Referencias

