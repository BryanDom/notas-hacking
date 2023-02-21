## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.
## Datos de acceso al nivel

-   user -> **bandit21**
-   Password -> NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
-   host -> **bandit.labs.overthewire.org**

## Solución
```
bandit21@bandit:~$ ls
bandit21@bandit:~$ ls -a
.  ..  .bash_logout  .bashrc  .prevpass  .profile
bandit21@bandit:~$ cd /etc/cron.d
bandit21@bandit:/etc/cron.d$ ls
cronjob_bandit15_root  cronjob_bandit22  cronjob_bandit24       e2scrub_all  sysstat
cronjob_bandit17_root  cronjob_bandit23  cronjob_bandit25_root  otw-tmp-dir
bandit21@bandit:/etc/cron.d$ cat cronjob_bandit22
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
bandit21@bandit:/etc/cron.d$  cat /usr/bin/cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@bandit:/etc/cron.d$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
bandit21@bandit:/etc/cron.d$
```
## Notas adicionales

#### Definiciones que entender

- **cron y crontab**: Programar o realizar una determinada y/o varias tareas en un determinado tiempo.

## Referencias
- https://www.redeszone.net/tutoriales/servidores/cron-crontab-linux-programar-tareas/