# LEVEL 29-30

## Objetivo
There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

Clone the repository and find the password for the next level.


## Datos acceso
ssh bandit29 @bandit.labs.overthewire.org -p 2220
tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
## Solucion
```bash
luego de clonar

bandit29@bandit:/tmp/tmp.SBlU3LKa4u$ ls
repo
bandit29@bandit:/tmp/tmp.SBlU3LKa4u$ cd repo
bandit29@bandit:/tmp/tmp.SBlU3LKa4u/repo$ ls -la
total 16
drwxrwxr-x 3 bandit29 bandit29 4096 Mar  3 00:56 .
drwx------ 3 bandit29 bandit29 4096 Mar  3 00:55 ..
drwxrwxr-x 8 bandit29 bandit29 4096 Mar  3 00:56 .git
-rw-rw-r-- 1 bandit29 bandit29  131 Mar  3 00:56 README.md
bandit29@bandit:/tmp/tmp.SBlU3LKa4u/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.
## credentials
- username: bandit30
- password: <no passwords in production!>
bandit29@bandit:/tmp/tmp.SBlU3LKa4u/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master
  remotes/origin/sploits-dev
bandit29@bandit:/tmp/tmp.SBlU3LKa4u/repo$ git checkout dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
Switched to a new branch 'dev'
bandit29@bandit:/tmp/tmp.SBlU3LKa4u/repo$ ls
code  README.md
bandit29@bandit:/tmp/tmp.SBlU3LKa4u/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.
## credentials
- username: bandit30
- password: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS

bandit29@bandit:/tmp/tmp.SBlU3LKa4u/repo$
```
## Notas adicionales
El comando "git branch -a" se utiliza en Git para mostrar una lista de todas las ramas (branch) en un repositorio, tanto las ramas locales como las ramas remotas.

La opción "-a" indica que se desea mostrar todas las ramas, incluidas las que no están activas en el repositorio local. Esto significa que el comando "git branch -a" muestra todas las ramas que se han creado en el repositorio, incluyendo aquellas que se han creado en repositorios remotos.

El comando "git checkout" se utiliza en Git para cambiar el estado de trabajo del repositorio a una determinada rama o commit.

Hay varias formas de usar el comando "git checkout", pero las más comunes son:

-   Cambiar a una rama existente: "git checkout (nombre-de-la-rama)". Este comando cambia la rama actual a la rama especificada. Los cambios que se realicen en este estado de trabajo se guardarán en la rama especificada.
    
-   Crear una nueva rama y cambiar a ella: "git checkout -b (nombre-de-la-nueva-rama)". Este comando crea una nueva rama con el nombre especificado y cambia a ella. Los cambios que se realicen en este estado de trabajo se guardarán en la nueva rama.
    
-   Cambiar a un commit específico: "git checkout (hash-del-commit)". Este comando cambia el estado de trabajo a un commit específico en lugar de una rama. Esto es útil si se desea ver el estado del repositorio en un momento anterior o revertir a un estado anterior del repositorio.
## Referencias

