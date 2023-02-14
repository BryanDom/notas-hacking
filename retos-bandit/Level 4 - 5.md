## Objetivo
The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

## Datos de acceso al nivel
-   user -> **bandit4**
-   Password -> 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
-   host -> **bandit.labs.overthewire.org**
## Solución
```
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere
bandit4@bandit:~/inhere$ ls
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ cat ./-file00
T߼B#6Kt36Xt��)
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
bandit4@bandit:~/inhere$
```
## Notas adicionales
#### Comandos linux

- **file** Con el comando file podemos saber el tipo de un fichero
## Referencias
- https://noviello.it/es/como-ver-el-tipo-de-archivo-con-el-comando-archivo-en-linux/
- https://tecnonautas.net/como-determinar-el-tipo-de-archivo-de-un-archivo-usando-linux/****
