## Objetivo

The password for the next level is stored in a file called **-** located in the home directory

## Datos de acceso al nivel

-   user -> **bandit1**
-   Password -> NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
-   host -> **bandit.labs.overthewire.org**

## Solución
```
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat -
^C
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ pwd
/home/bandit1
bandit1@bandit:~$ cat /home/bandit1/-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$
```
## Notas adicionales

#### Comandos linux
-**cat ./-** Para imprimir archivos nombrados - , se puede especificar la ruta.

-**cat < -** También redireccionar la salida. 

-**pwd** imprimir la ruta que tiene el directorio actual

-**cat ruta** Otra forma de imprimir es utilizando la ruta completa del archivo.

## Referencias
https://stackoverflow.com/questions/42187323/how-to-open-a-dashed-filename-using-terminal

Material del profesor.