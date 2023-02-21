## Objetivo

The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## Datos de acceso al nivel

-   user -> **bandit16**
-   Password -> JQttfApK4SeyHwDlI9SXGR50qclOAil1
-   host -> **bandit.labs.overthewire.org**

## Solución
```
bandit16@bandit:~$ nmap -p 31000-32000 localhostect localhost:31790
Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-21 18:07 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00010s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.05 seconds
bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 21 06:20:30 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 06:20:30 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 21 06:19:30 2023 GMT; NotAfter: Feb 21 06:20:30 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEXBJt0zANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjIxMDYxOTMwWhcNMjMwMjIxMDYyMDMwWjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCd
9XhmdGJmU9o7bfF1XlkI7KXKr0d3+W3cGZAryueO8Ox+GnSVZ6UUA6/j81Zn9yZY
J8O7R0iLwsl64z4IavxT78zzYsD/Uc3tSUo7AC7bi4sFLGiyQMegbBw2CT+lhduy
7yDF5dtzii7yk+LNBKAEP2x6fyXIPqL2o69hc6Rc1fJz713fD0vNbNxn09scGM0S
u2rRfCO2IczUrhbMMna+QfBMyQkn5Y6wswmVA2zMZUdF3J1d+R4oiyNsn0+F5o/m
hsMXizMjDZtZioOu6ZM6C30tgbzuaG3Jt/zysdBGFHmYLhMBkgsO5oEG/R9OzyZz
MnG/dfgEnwp7QuIjKFonAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQCR
+yllOIZJ98itYQvMR6oMMD/J3ACvmcPHhmNdyQX59/UcJkKlQD2s6N65ErC//bVp
LONgT3Bs+b5q9FK1DEIIGUlNln34e4Q5BQ7SvJFXVex9e/QIR6FR7uBrwCSbE03U
fHJ/oh5Q4bptB0OnoRir+b61y73bi68FMIpeuJ5vCQ2qqv2zyfx2xSZ2iJk6WK/r
64SSOtbKrm79MTjySF7Dq/VdJJIkfN4rxcIGzA+MRsb2AihWxFZkQ3dC3ZhGZSMP
wsSM0Kthicg5suIrO6HWJyDgE515H8dQO6B3PbrkS0zevcmgOarefJcuglf8bDaO
SQCWO+GKj/DYjEcp7evA
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 7FEA2EA3C2F15508E1931DA467B958699C7BA839453BDC1079FB24D72E6D6E43
    Session-ID-ctx:
    Resumption PSK: 7ABDC9F0F1E601489292D31C4BFF32222776AC8CCAF531D03D645FBFBF51B930A852D65936DCD86940107DE008F5385C
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 09 e8 08 6c e6 79 41 99-f0 10 77 90 1f 02 13 fc   ...l.yA...w.....
    0010 - 1c 9a 71 14 48 3b 33 4f-8b 21 fa 81 99 30 a5 23   ..q.H;3O.!...0.#
    0020 - 8e 78 49 ad 66 92 9a 0d-9a d4 10 3c e6 9a a5 9a   .xI.f......<....
    0030 - d5 be 20 79 85 08 88 8d-6e 2b f3 1b ed 90 d0 a7   .. y....n+......
    0040 - 7e 90 11 70 68 f5 85 3e-74 55 69 6b 16 be c8 2f   ~..ph..>tUik.../
    0050 - cd 02 29 f8 d8 32 2e 95-70 e9 26 c3 65 1b 07 98   ..)..2..p.&.e...
    0060 - bc fb 15 0c 9d 94 73 76-5c 39 3c 46 4c 50 9b a0   ......sv\9<FLP..
    0070 - a1 12 ab 98 74 95 cd 95-a5 4f 9d e8 fc 46 bb 83   ....t....O...F..
    0080 - 9c f5 58 21 e1 2e 9a 02-70 8f 6f ae 5c b9 6f d1   ..X!....p.o.\.o.
    0090 - 35 72 b6 9b 0f 14 ff 0f-0d fb a7 9a a3 e3 ec 7a   5r.............z
    00a0 - 50 c4 60 96 f4 1a 94 45-3e 07 3b 27 14 ee 91 f1   P.`....E>.;'....
    00b0 - 9c f5 4b 2a 38 3e 14 53-e8 99 50 d8 fd 13 74 55   ..K*8>.S..P...tU
    00c0 - 9b be 54 dd e0 5c 47 15-82 4a 2a 16 b7 e5 88 11   ..T..\G..J*.....

    Start Time: 1677002847
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 5655DC49169AB7D274FA47FF5F4348F1F0BB15323B4F1F973D4EF93F10C7AA53
    Session-ID-ctx:
    Resumption PSK: B8FB2D8E848A445A363DF17247CB3AB27E6892807010B27423BCA7283367014CD2004F9CDB7CD0A61348D72607D23A68
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 09 e8 08 6c e6 79 41 99-f0 10 77 90 1f 02 13 fc   ...l.yA...w.....
    0010 - 3d 5d 8c 3c fb e2 0d 7d-9a c5 32 d9 36 41 6d 9b   =].<...}..2.6Am.
    0020 - ad d3 f1 42 7a 6d f6 c3-81 69 1b 6a 4d 1b 5b 03   ...Bzm...i.jM.[.
    0030 - c2 12 62 aa fa 20 87 32-6d 3e cf 61 07 57 4e 90   ..b.. .2m>.a.WN.
    0040 - fc aa d9 52 a7 8c 0d 27-f8 29 c7 7d e6 6d 99 8e   ...R...'.).}.m..
    0050 - 05 63 df e6 32 ff e7 e2-3d 03 6c 67 f6 e4 46 4e   .c..2...=.lg..FN
    0060 - c1 81 75 ee 5d 7e ca c3-67 18 cb 14 90 44 77 9d   ..u.]~..g....Dw.
    0070 - 78 9b d8 bf d0 77 c8 86-2a 32 a2 df 02 2e 66 ab   x....w..*2....f.
    0080 - 30 fe f3 db d3 e5 fe 55-56 81 e4 a9 91 58 21 7f   0......UV....X!.
    0090 - 16 1a a6 0f bb 15 8b ce-38 b0 a9 dd 63 87 c8 2c   ........8...c..,
    00a0 - 9c b3 28 6e 47 9a 29 aa-47 eb 8c e8 cb e0 dc d7   ..(nG.).G.......
    00b0 - e9 c8 e4 56 3d 86 df 51-1a 21 d0 f0 78 26 65 b5   ...V=..Q.!..x&e.
    00c0 - 93 61 4b 9d c7 3a f9 9d-18 2b 76 48 82 2e 65 3b   .aK..:...+vH..e;

    Start Time: 1677002847
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

closed
bandit16@bandit:~$ exit

-----------------------PARTE 2--------------------------------------------------
C:\Users\brayan>notepad llave.txt

C:\Users\brayan>type llave.txt
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----
C:\Users\brayan>ssh -i llave.txt bandit17@bandit.labs.overthewire.org -p2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames


      ,----..            ,----,          .---.
     /   /   \         ,/   .`|         /. ./|
    /   .     :      ,`   .'  :     .--'.  ' ;
   .   /   ;.  \   ;    ;     /    /__./ \ : |
  .   ;   /  ` ; .'___,/    ,' .--'.  '   \' .
  ;   |  ; \ ; | |    :     | /___/ \ |    ' '
  |   :  | ; | ' ;    |.';  ; ;   \  \;      :
  .   |  ' ' ' : `----'  |  |  \   ;  `      |
  '   ;  \; /  |     '   :  ;   .   \    .\  ;
   \   \  ',  /      |   |  '    \   \   ' \ |
    ;   :    /       '   :  |     :   '  |--"
     \   \ .'        ;   |.'       \   \ ;
  www. `---` ver     '---' he       '---" ire.org


Welcome to OverTheWire!

If you find any problems, please report them to the #wargames channel on
discord or IRC.

--[ Playing the games ]--

  This machine might hold several wargames.
  If you are playing "somegame", then:

    * USERNAMES are somegame0, somegame1, ...
    * Most LEVELS are stored in /somegame/.
    * PASSWORDS for each level are stored in /etc/somegame_pass/.

  Write-access to homedirectories is disabled. It is advised to create a
  working directory with a hard-to-guess name in /tmp/.  You can use the
  command "mktemp -d" in order to generate a random and hard to guess
  directory in /tmp/.  Read-access to both /tmp/ is disabled and to /proc
  restricted so that users cannot snoop on eachother. Files and directories
  with easily guessable or short names will be periodically deleted! The /tmp
  directory is regularly wiped.
  Please play nice:

    * don't leave orphan processes running
    * don't leave exploit-files laying around
    * don't annoy other players
    * don't post passwords or spoilers
    * again, DONT POST SPOILERS!
      This includes writeups of your solution on your blog or website!

--[ Tips ]--

  This machine has a 64bit processor and many security-features enabled
  by default, although ASLR has been switched off.  The following
  compiler flags might be interesting:

    -m32                    compile for 32bit
    -fno-stack-protector    disable ProPolice
    -Wl,-z,norelro          disable relro

  In addition, the execstack tool can be used to flag the stack as
  executable on ELF binaries.

  Finally, network-access is limited for most levels by a local
  firewall.

--[ Tools ]--

 For your convenience we have installed a few useful tools which you can find
 in the following locations:

    * gef (https://github.com/hugsy/gef) in /opt/gef/
    * pwndbg (https://github.com/pwndbg/pwndbg) in /opt/pwndbg/
    * peda (https://github.com/longld/peda.git) in /opt/peda/
    * gdbinit (https://github.com/gdbinit/Gdbinit) in /opt/gdbinit/
    * pwntools (https://github.com/Gallopsled/pwntools)
    * radare2 (http://www.radare.org/)

 Both python2 and python3 are installed.

--[ More information ]--

  For more information regarding individual wargames, visit
  http://www.overthewire.org/wargames/

  For support, questions or comments, contact us on discord or IRC.

  Enjoy your stay!

bandit17@bandit:~$ ls
passwords.new  passwords.old
bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
bandit17@bandit:~$
```
## Notas adicionales
#### Definiciones que entender
- **Notepad**: crea o abre un archivo de txt con el nombre que le pasemos, (Ej. notepad llave.txt)

#### Comandos Linux Utilizados 

- **nmap**: Comando en el cual permite realizar un escaneo a los puertos.

- **-p**: Comando en el cual va indicar el rango de puertos a escanear.

## Referencias
- https://en.wikipedia.org/wiki/Port_scanner
- https://rm-rf.es/nmap-linux-uso-ejemplos/#:~:text=Nmap%20(Abreviatura%20de%20Network%20Mapper,un%20inventario%20de%20red%2C%20etc.