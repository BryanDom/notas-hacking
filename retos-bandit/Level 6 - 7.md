## Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

-   owned by user bandit7
-   owned by group bandit6
-   33 bytes in size
## Datos de acceso al nivel
-   user -> **bandit6**
-   Password -> P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
-   host -> **bandit.labs.overthewire.org**
## Solución
```
bandit6@bandit:~$ ls
bandit6@bandit:~$ ls -a
.  ..  .bash_logout  .bashrc  .profile
bandit6@bandit:~$ ls -la
total 20
drwxr-xr-x  2 root root 4096 Jan 11 19:18 .
drwxr-xr-x 70 root root 4096 Jan 11 19:19 ..
-rw-r--r--  1 root root  220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root root 3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root root  807 Jan  6  2022 .profile
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:~$
```
## Notas adicionales
#### Comandos Linux Utilizados

- **find / -user bandit7 -group bandit6 -size 33c 2>/dev/null** : En el siguiente comando, se usa find para encontrar una archivo, de un usuario, grupo y tamaño específico, en el cual se nos esta indicando en el *objetivo* y además los archivos o directorios que no se pudieron revisar son redirigidos como errores.

- **2>/dev/null**: Comando en el cual indica los errores que no se pueden revisar.
## Referencias
- https://linuxhint.com/two-dev-null-command-purpose/
- https://askubuntu.com/questions/350208/what-does-2-dev-null-mean