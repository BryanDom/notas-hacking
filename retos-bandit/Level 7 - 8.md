
## Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**
## Datos de acceso al nivel
-   user -> **bandit7**
-   Password -> z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
-   host -> **bandit.labs.overthewire.org**
## Solución
```
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ wc data.txt
  98567  197133 4184396 data.txt
bandit7@bandit:~$ grep millionth data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$
```
## Notas adicionales
#### Comandos Linux Utilizados
- **wc**: Es un comando que se utiliza para realizar diferentes conteos desde la entrada estándar, ya sea de palabras, caracteres o saltos de líneas**.
- **grep**: Este comando nos permite buscar una palabra o patron, e imprimir las líneas que la contienen.
## Referencias
- https://es.wikipedia.org/wiki/Wc_(Unix)#:~:text=wc%20(word%20count)%20es%20un,caracteres%20o%20saltos%20de%20l%C3%ADneas.
- https://www.maketecheasier.com/what-is-grep-and-uses/