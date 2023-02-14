
## Objetivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

-   human-readable
-   1033 bytes in size
-   not executable
## Datos de acceso al nivel
-   user -> **bandit5**
-   Password -> lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
-   host -> **bandit.labs.overthewire.org**
## Solución
```
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
bandit5@bandit:~/inhere$ file ./*
./maybehere00: directory
./maybehere01: directory
./maybehere02: directory
./maybehere03: directory
./maybehere04: directory
./maybehere05: directory
./maybehere06: directory
./maybehere07: directory
./maybehere08: directory
./maybehere09: directory
./maybehere10: directory
./maybehere11: directory
./maybehere12: directory
./maybehere13: directory
./maybehere14: directory
./maybehere15: directory
./maybehere16: directory
./maybehere17: directory
./maybehere18: directory
./maybehere19: directory
bandit5@bandit:~/inhere$ find . -readable -type f -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
bandit5@bandit:~/inhere$
```
## Notas adicionales
#### Comandos linux

- **find** Permite encontrar un archivo o directorio, con los parámetros dados.

- **find . -readable -type f - size 1033c** El comando indica que se busca un archivo, que tiene un tamaño de 1033 caracteres y que sea de tipo de lectura, ademas el **-f** devuelve true si es un archivo ordinario y existente.

## Referencias
- https://www.ionos.mx/digitalguide/servidores/configuracion/comando-linux-find/
- https://www.hostinger.mx/tutoriales/como-usar-comando-find-locate-en-linux/#:~:text=Utilizar%20el%20comando%20find%20en%20Linux%20para%20buscar%20archivos%20por,r%C3%A1pidas%20en%20todo%20el%20sistema.