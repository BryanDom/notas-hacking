## Objetivo

There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

Clone the repository and find the password for the next level.

## Datos de acceso al nivel

-   User -> **bandit28**
-   Password -> AVanL161y9rsbcJIsFHuw35rjaOM19nR
-   Host -> **bandit.labs.overthewire.org**

## Solución
```
bandit28@bandit:~$ ls
bandit28@bandit:~$ mkdir /tmp/bryan16ds
bandit28@bandit:~$ cd /tmp/bryan16ds
bandit28@bandit:/tmp/bryan16ds$ git clone ssh://bandit28 git@localhost:2220/home/bandit28-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit28/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit28/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit28-git@localhost's password:
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 9 (delta 2), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (9/9), done.
Resolving deltas: 100% (2/2), done.

bandit28@bandit:/tmp/bryan16ds$ ls
repo
bandit28@bandit:/tmp/bryan16ds$ cd repo
bandit28@bandit:/tmp/bryan16ds/repo$ ls -la
total 16
drwxrwxr-x 3 bandit28 bandit28 4096 Feb 25 17:03 .
drwxrwxr-x 3 bandit28 bandit28 4096 Feb 25 17:03 ..
drwxrwxr-x 8 bandit28 bandit28 4096 Feb 25 17:03 .git
-rw-rw-r-- 1 bandit28 bandit28  111 Feb 25 17:03 README.md
bandit28@bandit:/tmp/bryan16ds/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx

bandit28@bandit:/tmp/bryan16ds/repo$ git log
commit 104db85a904e9691ff22aafe1a96124c88f75afa (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    fix info leak

commit 6c3c5e485cc531e5d52c321587ce1103833ab7c3
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    add missing data

commit cd3b97ef95879ec34df0d6c82f2a96d552f0e56c
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    initial commit of README.md
bandit28@bandit:/tmp/bryan16ds/repo$ git show 104db85a904e9691ff22aafe1a96124c88f75afa
commit 104db85a904e9691ff22aafe1a96124c88f75afa (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    fix info leak

diff --git a/README.md b/README.md
index b302105..5c6457b 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for level29 of bandit.
 ## credentials

 - username: bandit29
-- password: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
+- password: xxxxxxxxxx

bandit28@bandit:/tmp/bryan16ds/repo$ git show 6c3c5e485cc531e5d52c321587ce1103833ab7c3
commit 6c3c5e485cc531e5d52c321587ce1103833ab7c3
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    add missing data

diff --git a/README.md b/README.md
index 7ba2d2f..b302105 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for level29 of bandit.
 ## credentials

 - username: bandit29
-- password: <TBD>
+- password: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S

bandit28@bandit:/tmp/bryan16ds/repo$
```
## Notas adicionales

#### Definiciones que entender
- **git log**: Este comando de git, nos sirve para ver los registros y/o historial que contiene el repositorio del git que clonamos. 

- **git show**: Este comando del git, nos permite y/o sirve para poder ver los registros obtenidos con git log.


## Referencias
- https://careerkarma.com/blog/git-log/#:~:text=The%20git%20log%20command%20shows,the%20history%20of%20a%20repository.
- https://www.atlassian.com/git/tutorials/git-show#:~:text=What%20is%20git%2Dshow%3F,of%20objects%20in%20a%20tree.