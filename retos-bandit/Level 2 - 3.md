
## Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory
## Datos de acceso al nivel
-   user -> **bandit2**
-   Password -> rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
-   host -> **bandit.labs.overthewire.org**
## Solución
```
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces in this filename
cat: spaces: No such file or directory
cat: in: No such file or directory
cat: this: No such file or directory
cat: filename: No such file or directory
bandit2@bandit:~$ cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$
```
## Notas adicionales
- Un archivo que tiene el nombre con espacio puede ser seleccionado con solamente encerrar el nombre entre comillas dobles o tambien otra forma es escribir el inicio del nombre y el primer esapcio poner el directorio "\".
## Referencias
- https://learn.microsoft.com/en-us/troubleshoot/windows-server/deployment/filenames-with-spaces-require-quotation-mark
- https://elblogdeliher.com/como-abrir-un-directorio-que-tiene-espacio-en-su-nombre-en-ubuntu/