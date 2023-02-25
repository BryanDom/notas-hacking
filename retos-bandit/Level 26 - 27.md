## Objetivo

Good job getting a shell! Now hurry and grab the password for bandit27!

## Datos de acceso al nivel

-   User -> **bandit26**
-   Password -> c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
-   Host -> **bandit.labs.overthewire.org**

## Solución
```
C:\Users\brayan>ssh bandit26@bandit.labs.overthewire.org -p2220
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
Connection to bandit.labs.overthewire.org closed.

C:\Users\brayan>ssh bandit26@bandit.labs.overthewire.org -p2220
v

:set shell=/bin/bash

:shell

bandit26@bandit:~$ ls
bandit27-do  text.txt
bandit26@bandit:~$ ls -la
total 44
drwxr-xr-x  3 root     root      4096 Feb 21 22:03 .
drwxr-xr-x 70 root     root      4096 Feb 21 22:04 ..
-rwsr-x---  1 bandit27 bandit26 14876 Feb 21 22:03 bandit27-do
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
drwxr-xr-x  2 root     root      4096 Feb 21 22:03 .ssh
-rw-r-----  1 bandit26 bandit26   258 Feb 21 22:03 text.txt
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
bandit26@bandit:~$
```

## Notas adicionales
#### Definiciones que entender

- **ssh bandit26@bandit.labs.overthewire.org -p2220**: Al momento de teclear este comando recordemos que el bandit26 no te permitira entrar al servidor asi que aplicamos lo mismo que en el reto anterior, ¿Que cosa?, tenemos que entrar pero con la pantalla reducida, en el cmd donde estemos trabajando nos dira que no se a cargado completamente las cosas por completo y ahi es donde oprimiremos la tecla v y luego teclearemos el siguiente comando para entrar directo al shell de bandit26 **:set shell=/bin/bash** y luego el otro comando **:shell** y listo, asi podemos manejarnos dentro de la terminal del reto.

## Referencias
- https://mayadevbe.me/posts/overthewire/bandit/level27/