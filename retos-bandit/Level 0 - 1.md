
## Objetivo
The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## Datos de acceso al nivel

-   user -> **bandit0**
-   Password -> **bandit0**
-   host -> **bandit.labs.overthewire.org**

## Solución
```
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
bandit0@bandit:~$
```
## Notas adicionales

#### Comandos linux
**cat** - Mostrar el contenido de un archivo de texto.

## Referencias
Material proporcionado por el profesor.