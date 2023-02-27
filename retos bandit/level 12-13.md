# LEVEL 12-23

## Objetivo
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## Datos acceso
ssh bandit12 @bandit.labs.overthewire.org -p 2220
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

## Solucion
```bash
bandit12@bandit:~$ xxd -r data.txt | file -
/dev/stdin: gzip compressed data, was "data2.bin", last modified: Wed Jan 11 19:18:38 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt | zcat |file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat |file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | file -
/dev/stdin: gzip compressed data, was "data9.bin", last modified: Wed Jan 11 19:18:38 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat | file -
/dev/stdin: ASCII text
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
bandit12@bandit:~$

```

## Notas adicionales
xxd -r quita vaciado hexadecimal

The zcat command **allows the user to expand and view a compressed file without uncompressing that file**. The zcat command does not rename the expanded file or remove the . Z extension. The zcat command writes the expanded output to standard output. archivos .gz gzip

_bzcat_ (or _bzip2 -dc)_ decompresses all specified files to the standard output.

_bzip2_ will read arguments from the environment variables _BZIP2_ and _BZIP,_ in that order, and will process them before any arguments read from the command line. This gives a convenient way to supply default arguments.

tar xO descomprime archivos .tar
  



## Referencias

https://www.ibm.com/docs/en/aix/7.1?topic=z-zcat-command#:~:text=The%20zcat%20command%20allows%20the,expanded%20output%20to%20standard%20output. gzip

[https://www.commandlinux.com/man-page/man1/bzcat.1.html](https://www.commandlinux.com/man-page/man1/bzcat.1.html).bz2 bzip2