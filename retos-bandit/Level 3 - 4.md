
## Objetivo
The password for the next level is stored in a hidden file in the **inhere** directory.
## Datos de acceso al nivel
-   user -> **bandit3**
-   Password -> aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
-   host -> **bandit.labs.overthewire.org**
## Solución
```
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
bandit3@bandit:~/inhere$
```
## Notas adicionales
#### Comandos linux
- **ls -a** Permite listar archivos y muestra los que están ocultos.
## Referencias
- https://cambiatealinux.com/mostrar-los-archivos-ocultos-en-linux#:~:text=Todos%20los%20exploradores%20de%20archivos,se%20muestran%20los%20archivos%20ocultos.