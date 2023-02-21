## Objetivo
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

## Datos de acceso al nivel
-   user -> **bandit19**
-   Password -> awhqfNnAbc1naukrpqDYcF95h7HoMTrC
-   host -> **bandit.labs.overthewire.org**
## Solución
```
bandit19@bandit:~$ ls
bandit20-do
bandit19@bandit:~$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Jan 11 19:18 .
drwxr-xr-x 70 root     root      4096 Jan 11 19:19 ..
-rwsr-x---  1 bandit20 bandit19 14876 Jan 11 19:18 bandit20-do
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit19@bandit:~$
```
## Notas adicionales

#### Definiciones que entender
- **Setuid y setgid**: Permiten a los usuarios ejecutar un ejecutable con los permisos del sistema de archivos del propietario o grupo del ejecutable respectivamente y cambiar el comportamiento en los directorios, a menudo se utilizan para permitir que los usuarios de un sistema informático ejecuten programas con privilegios elevados temporalmente para realizar una tarea específica.

## Referencias
- https://en.wikipedia.org/wiki/Setuid