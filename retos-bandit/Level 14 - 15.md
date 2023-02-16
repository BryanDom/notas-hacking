## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.
## Datos de acceso al nivel
-   user -> **bandit14**
-   Password -> fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
-   host -> **bandit.labs.overthewire.org**
## Solución
```
bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

^C
bandit14@bandit:~$
```
## Notas adicionales

#### Definiciones que entender
Los puertos pueden configurarse para que realicen procesos.

#### Comandos Linux Utilizados

- **nc**: Comando en el cual podemos conectarnos a los puertos TCP/UDP de un host. 

- **Nota Extra**: **-v** Este comando también lo hubieramos podido utilizar ya que puede mostrar información acerca de la conexión.

## Referencias
- https://ccia.esei.uvigo.es/docencia/SCS/1011/practicas/practica-1/index.html#:~:text=interfaz%20de%20SOCKETS.-,Comando%20nc%2Fnetcat,UDP)%20de%20la%20m%C3%A1quina%20local.
- https://en.wikipedia.org/wiki/Port_(computer_networking)
- https://en.wikipedia.org/wiki/Localhost
- https://www.fing.edu.uy/inco/cursos/sistoper/recursosLaboratorio/tutorial0.pdf