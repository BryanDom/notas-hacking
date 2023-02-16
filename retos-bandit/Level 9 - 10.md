
## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
## Datos de acceso al nivel
-   user -> **bandit9**
-   Password -> EN632PlfYiZbn3PhVK3XOGSlNInNE00t
-   host -> **bandit.labs.overthewire.org**
## Solución
```
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ file ./*
./data.txt: data
bandit9@bandit:~$ strings data.txt | grep ==
c========== the
h;========== password
========== isT
n.E========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit9@bandit:~$
```
## Notas adicionales
#### Comandos Linux Utilizados

- **strings**: Permite obtener los caracteres legibles de un archivo, de un archivo binario no legible.
- **grep**: Busca en un archivo un patrón particular de caracteres y muestra todas las líneas que contienen ese patrón.
## Referencias
- https://www.geeksforgeeks.org/grep-command-in-unixlinux/
- https://www.javatpoint.com/linux-strings-command#:~:text=Linux%20strings%20command%20is%20used,text%20from%20an%20executable%20file.