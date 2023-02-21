## Objetivo
The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.
## Datos de acceso al nivel
-   user -> **bandit18**
-   Password -> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
-   host -> **bandit.labs.overthewire.org**
## Solución
```
C:\Users\brayan>ssh  bandit18@bandit.labs.overthewire.org -p 2220 ls
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:
readme

C:\Users\brayan>ssh  bandit18@bandit.labs.overthewire.org -p 2220 cat readme
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:
awhqfNnAbc1naukrpqDYcF95h7HoMTrC
C:\Users\brayan>
```
## Notas adicionales

#### Definiciones que entender
- Madar un **ls** y/o un **cat** junto con la conexión (cualquiera), se ejecutara estos comandos antes de que se cierre la sesión como nos estaba pasando.

## Referencias
- https://cambiatealinux.com/acceder-por-ssh-directamente-a-un-directorio-del-servidor