
## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
## Datos de acceso al nivel
-   user -> **bandit8**
-   Password -> TESKZC0XvTetK0S9xNwm25STk5iWrBvP
-   host -> **bandit.labs.overthewire.org**
## Solución
```
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ wc data.txt
 1001  1001 33033 data.txt
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$
```
## Notas adicionales
#### Comandos Linux Utilizados

- **sort**: Comando en el cual permite ordenar las lineas de texto.

- **uniq**: Comando en el cual permite filtrar las lineas de texto. 

- **-u**: Comando en el cual muestra solo las lineas unicas

- **|**: Comando en el cual envía información de un comando a otro
## Referencias
- https://www.ibidemgroup.com/edu/tutorial-sort-linux-unix/#:~:text=M%C3%A1s%20informaci%C3%B3n-,%C2%BFQu%C3%A9%20es%20el%20comando%20sort%3F,y%20tambi%C3%A9n%20puede%20eliminar%20duplicados
- https://nksistemas.com/comando-uniq-de-linux-explicado-con-ejemplos/
- https://axarnet.es/blog/comandos-linux