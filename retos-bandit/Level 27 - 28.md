## Objetivo

There is a git repository at `ssh://bandit27-git@localhost/home/bandit27-git/repo`. The password for the user `bandit27-git` is the same as for the user `bandit27`.

Clone the repository and find the password for the next level.

## Datos de acceso al nivel

-   User -> **bandit27**
-   Password -> YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
-   Host -> **bandit.labs.overthewire.org**

## Solución
```
bandit27@bandit:~$ ls
bandit27@bandit:~$ ls -la
total 20
drwxr-xr-x  2 root root 4096 Feb 21 22:02 .
drwxr-xr-x 70 root root 4096 Feb 21 22:04 ..
-rw-r--r--  1 root root  220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root root 3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root root  807 Jan  6  2022 .profile
bandit27@bandit:~$ mkdir /tmp/bryands
bandit27@bandit:~$ cd /tmp/bryands
bandit27@bandit:/tmp/bryands$ git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit27/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit27/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit27-git@localhost's password:YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.

bandit27@bandit:/tmp/bryands$ ls
repo

bandit27@bandit:/tmp/bryands$ cd repo
bandit27@bandit:/tmp/bryands/repo$ ls -la
total 16
drwxrwxr-x 3 bandit27 bandit27 4096 Feb 25 16:29 .
drwxrwxr-x 3 bandit27 bandit27 4096 Feb 25 16:29 ..
drwxrwxr-x 8 bandit27 bandit27 4096 Feb 25 16:29 .git
-rw-rw-r-- 1 bandit27 bandit27   68 Feb 25 16:29 README
bandit27@bandit:/tmp/bryands/repo$ cat README
The password to the next level is: AVanL161y9rsbcJIsFHuw35rjaOM19nR
bandit27@bandit:/tmp/bryands/repo$
```
## Notas adicionales

#### Definiciones que entender
- **git clone**: Comando que sirve para descargar y/o clonar un repositorio, claro indicando su respectivo link del repo y el puerto (2220).

## Referencias
- https://docs.github.com/es/repositories/creating-and-managing-repositories/cloning-a-repository