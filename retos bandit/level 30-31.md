# LEVEL 30-31

## Objetivo
There is a git repository at `ssh://bandit30-git@localhost:2220/home/bandit30-git/repo`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.


## Datos acceso
ssh bandit30 @bandit.labs.overthewire.org -p 2220
xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
## Solucion
```bash
luego de clonar
bandit30@bandit:/tmp/tmp.A0QzKZINaR$ ls
repo
bandit30@bandit:/tmp/tmp.A0QzKZINaR$ cat repo
cat: repo: Is a directory
bandit30@bandit:/tmp/tmp.A0QzKZINaR$ cd repo
bandit30@bandit:/tmp/tmp.A0QzKZINaR/repo$ ls
README.md
bandit30@bandit:/tmp/tmp.A0QzKZINaR/repo$ cat README.md
just an epmty file... muahaha
bandit30@bandit:/tmp/tmp.A0QzKZINaR/repo$ git tag
secret
bandit30@bandit:/tmp/tmp.A0QzKZINaR/repo$  git show secret
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
bandit30@bandit:/tmp/tmp.A0QzKZINaR/repo$
```
## Notas adicionales
El comando "git tag" se utiliza en Git para etiquetar una confirmación (commit) específica en un repositorio Git. Las etiquetas son referencias humanas y fáciles de recordar que se utilizan para marcar versiones específicas de un proyecto.

El comando "git show" se utiliza en Git para mostrar información detallada sobre un objeto Git específico, como un commit, una rama o una etiqueta. El comando muestra información como el autor del objeto, la fecha y hora en que se creó y cualquier mensaje asociado con él. También muestra los cambios realizados en el objeto, si es un commit.
## Referencias

