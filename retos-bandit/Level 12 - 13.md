## Objetivo
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)
## Datos de acceso al nivel
-   user -> **bandit12**
-   Password -> JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
-   host -> **bandit.labs.overthewire.org**
## Solución
```
bandit12@bandit:~$ mkdir /tmp/brayan123
bandit12@bandit:~$ cp data.txt /tmp/brayan123
bandit12@bandit:~$ cd /tmp/brayan123
bandit12@bandit:/tmp/brayan123$ ls
data.txt
bandit12@bandit:/tmp/brayan123$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
bandit12@bandit:/tmp/brayan123$
```
## Notas adicionales

#### Definiciones que entender
Una vez que el archivo esté en binario, se descomprime según el tipo de comprensión.

**Nota Extra**: El comando file ayuda a saber cómo está comprimido.

#### Comandos Linux Utilizados

- **xxd**: Comando en el cual crea un volcado hexadecimal de un archivo, en el cual este comando también puede convertir un volcado hexadecimal de nuevo a su forma binaria inicial.

- **-r**: Comando en el cual transforma de hexadecimal a binario.

- **tar xO**: Comando en el cual nos permite comprimir archivos y directorios en memoria, equivalente a tar.

- **bzcat**: Comando en el cual permite comprimir archivos y directorios en memoria, equivalente a bzip2.

- **zcat**: Comando en el cual es de gran utilidad de líneas de comandos para ver el contenido de un archivo comprimido sin descomprimirlo, equivalente a gzip.

## Referencias
- https://francisconi.org/linux/comandos/xxd
- http://www.w3big.com/es/linux/linux-comm-tar.html#gsc.tab=0
- https://www.solvetic.com/tutoriales/article/3683-comandos-gzip-gunzip-y-zcat-en-linux/#:~:text=Su%20uso%20es%20id%C3%A9ntico%20a,de%20si%20es%20o%20no%20
- https://www.commandlinux.com/man-page/man1/bzcat.1.html