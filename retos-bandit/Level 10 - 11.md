
## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
## Datos de acceso al nivel

-   user -> **bandit10**
-   Password -> G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
-   host -> **bandit.labs.overthewire.org**

## Solución
```
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ base64 -d data.txt
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$
```
## Notas adicionales
#### Comandos Linux Utilizados

- **base64**:  comando en el cual permite codificar o descodificar en base64. 
- **-d**: comando que indica que se va a decodificar. 
- **-e**: (comando extra por si a caso) en el cual indica que se va a codificar.
## Referencias
- https://rm-rf.es/codificar-y-descodificar-base64-desde-bash/