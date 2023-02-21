## Objetivo
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

**NOTE:** Try connecting to your own network daemon to see if it works as you think

## Datos de acceso al nivel

-   user -> **bandit20**
-   Password -> VxCazJaVykI6W36BkBU0mJTCM8rR95XT
-   host -> **bandit.labs.overthewire.org**

## Solución
Terminal 1:
```
bandit20@bandit:~$ nc -lnvp 2020 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[2] 1289787
bandit20@bandit:~$ Listening on 0.0.0.0 2020
Connection received on 127.0.0.1 40310
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
^C
[1]-  Done                    nc -lnvp 2020 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit20@bandit:~$
```

Terminal 2:
```
bandit20@bandit:~$ ./suconnect 2020
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
bandit20@bandit:~$
```
## Notas adicionales

#### Definiciones que entender

Estamos abriendo un puerto "2020", en el cual por "defecto" le estamos pasando la contraseña para conectarse desde otra termina, es decir, en una terminal abrimos el puerto y en otra terminal nos conectamos.

#### Comandos Linux Utilizados 
- **nc**: Comando en el cual se  puede conectar a los puertos **TCP/UDP** de un host. 

- **-l**: Comando que sirve para que Netcat abra un puerto y se mantenga ala escucha. Se aceptará una única conexión de un único cliente antes de cerrarse. 

-  **-v**: Comando que se usa para mostrar información acerca de la conexión.

- **-p**: Comando que permite especificar el puerto al que conectarse. 

## Referencias
- https://ccia.esei.uvigo.es/docencia/SCS/1011/practicas/practica-1/index.html#:~:text=interfaz%20de%20SOCKETS.-,Comando%20nc%2Fnetcat,UDP)%20de%20la%20m%C3%A1quina%20local.
- https://www.neoguias.com/comando-nc/