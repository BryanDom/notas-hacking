## Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
## Datos de acceso al nivel

-   user -> **bandit11**
-   Password -> 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
-   host -> **bandit.labs.overthewire.org**

## Solución
```
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m
> '
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
bandit11@bandit:~$
```
## Notas adicionales
#### Definiciones que entender
ROT13 es un cifrado de sustitución de letra simple que reemplaza una letra con la letra 13 después de ella en el alfabeto.

#### Comandos Linux Utilizados
**tr**: Comando en el cual permite modificar cadenas, sustituir carácter y aplicar los respectivos cifrados.

## Referencias
- https://geekland.eu/uso-del-comando-tr-en-linux-y-unix-con-ejemplos/
- https://www.xataka.com/historia-tecnologica/asi-rot13-algoritmo-cifrado-simple-que-ha-revivido-para-ocultar-spoilers