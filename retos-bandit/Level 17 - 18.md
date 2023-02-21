## Objetivo
There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

**NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19**

## Datos de acceso al nivel

-   user -> **bandit17**
-   Password -> VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
-   host -> **bandit.labs.overthewire.org**

## Solución
```
bandit17@bandit:~$ ls
passwords.new  passwords.old
bandit17@bandit:~$ ls -a
.  ..  .bandit16.password  .bash_logout  .bashrc  passwords.new  passwords.old  .profile  .ssh
bandit17@bandit:~$ ls -la
total 36
drwxr-xr-x  3 root     root     4096 Jan 11 19:18 .
drwxr-xr-x 70 root     root     4096 Jan 11 19:19 ..
-rw-r-----  1 bandit17 bandit17   33 Jan 11 19:18 .bandit16.password
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit18 bandit17 3300 Jan 11 19:18 passwords.new
-rw-r-----  1 bandit18 bandit17 3300 Jan 11 19:18 passwords.old
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
drwxr-xr-x  2 root     root     4096 Jan 11 19:18 .ssh
bandit17@bandit:~$ diff passwords.old passwords.new
42c42
< 810zq8IK64u5A9Lb2ibdTGBtlcSZsoe8
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
bandit17@bandit:~$ diff passwords.old passwords.new --color
42c42
< 810zq8IK64u5A9Lb2ibdTGBtlcSZsoe8
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
bandit17@bandit:~$
```
## Notas adicionales
#### Comandos Linux Utilizados 
- **diff**: Comando en el cual compara las diferencias entre ficheros línea a línea.

- **--color**: Comando que sirve para colorear la salida del comando y/o comparación que en este caso estamos haciendo.

## Referencias
- https://kinsta.com/es/blog/linux-comandos/
- https://geekland.eu/comparar-directorios-y-archivos-comando-diff-linux/#:~:text=diff%3A%20Es%20la%20utilidad%20para,est%C3%A1n%20dentro%20del%20directorio%20analizado.
