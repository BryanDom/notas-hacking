## Objetivo

There is a git repository at `ssh://bandit31-git@localhost/home/bandit31-git/repo`. The password for the user `bandit31-git` is the same as for the user `bandit31`.

Clone the repository and find the password for the next level.

## Datos de acceso al nivel

-   User -> **bandit31**
-   Password -> OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
-   Host -> **bandit.labs.overthewire.org**

## Solución
```
bandit31@bandit:~$ mkdir /tmp/brayan2
bandit31@bandit:~$ cd /tmp/brayan2
bandit31@bandit:/tmp/brayan2$ git clone ssh://bandit31-git@localhost/home/bandit31-git/repo
Cloning into 'repo'...
The authenticity of host 'localhost (127.0.0.1)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).

                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

!!! You are trying to log into this SSH server on port 22, which is not intended.

bandit31-git@localhost: Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
bandit31@bandit:/tmp/brayan2$ git clone ssh://bandit31-git@localhost:2220/home/bandit31-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames
bandit31-git@localhost's password:
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (4/4), done.
bandit31@bandit:/tmp/brayan2$ ls
repo
bandit31@bandit:/tmp/brayan2$ cd repo
bandit31@bandit:/tmp/brayan2/repo$ ls
README.md
bandit31@bandit:/tmp/brayan2/repo$ cat README.md
This time your task is to push a file to the remote repository.

Details:
    File name: key.txt
    Content: 'May I come in?'
    Branch: master

bandit31@bandit:/tmp/brayan2/repo$ echo ''May I come in?'' > key.txt
bandit31@bandit:/tmp/brayan2/repo$ cat key.txt
May I come in?
bandit31@bandit:/tmp/brayan2/repo$ ls -la
total 24
drwxrwxr-x 3 bandit31 bandit31 4096 Feb 25 19:01 .
drwxrwxr-x 3 bandit31 bandit31 4096 Feb 25 18:58 ..
drwxrwxr-x 8 bandit31 bandit31 4096 Feb 25 18:58 .git
-rw-rw-r-- 1 bandit31 bandit31    6 Feb 25 18:58 .gitignore
-rw-rw-r-- 1 bandit31 bandit31   15 Feb 25 19:01 key.txt
-rw-rw-r-- 1 bandit31 bandit31  147 Feb 25 18:58 README.md
bandit31@bandit:/tmp/brayan2/repo$ rm .gitignore
bandit31@bandit:/tmp/brayan2/repo$ git add key.txt
bandit31@bandit:/tmp/brayan2/repo$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   key.txt

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    .gitignore

bandit31@bandit:/tmp/brayan2/repo$ git commit -m "brayan"
[master 2507ec0] brayan
 1 file changed, 1 insertion(+)
 create mode 100644 key.txt
bandit31@bandit:/tmp/brayan2/repo$ git log
commit 2507ec0344a75ff2f3c862936ee98d807b909575 (HEAD -> master)
Author: bandit31 <bandit31@overthewire.org>
Date:   Sat Feb 25 19:03:40 2023 +0000

    brayan

commit 5c1d06a02163d3224e06f00ca0bbfe1c2768ce00 (origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:14 2023 +0000

    initial commit
bandit31@bandit:/tmp/brayan2/repo$ git push

rmCBvG56y58BXzv98yZGdO7ATVL5dW8y

The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password:
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 320 bytes | 320.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: ### Attempting to validate files... ####
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
remote: Well done! Here is the password for the next level:
remote: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
To ssh://localhost:2220/home/bandit31-git/repo
 ! [remote rejected] master -> master (pre-receive hook declined)
error: failed to push some refs to 'ssh://localhost:2220/home/bandit31-git/repo'
bandit31@bandit:/tmp/brayan2/repo$
```
## Notas adicionales

#### Definiciones que entender
- **rm**: Para desasernos del archivo get ignore, para asi poder hacer el "add" sin necesidad de realizar un "git add -f".
- **git status**: Comando muestra el estado del directorio de trabajo y el área de ensayo. Le permite ver qué cambios se han realizado, cuáles no y qué archivos no están siendo rastreados por Git.

## Referencias
- https://www.ibm.com/docs/es/aix/7.1?topic=files-deleting-rm-command

- https://www.atlassian.com/git/tutorials/inspecting-a-repository#:~:text=The%20git%20status%20command%20displays,regarding%20the%20committed%20project%20history.