## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**
## Datos de acceso al nivel
-   user -> **bandit14**
-   Password -> jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
-   host -> **bandit.labs.overthewire.org**
## Solución
```
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 15 15:53:14 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 15 15:53:14 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 15 15:52:14 2023 GMT; NotAfter: Feb 15 15:53:14 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEWQQUSzANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjE1MTU1MjE0WhcNMjMwMjE1MTU1MzE0WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDG
GfFvOWmaL5zjdsa4Df/R+w0TnZiTHCp8qOWzkTeTVb+3onMlpNJ7/VzC/XwvzRoV
CgDC4F/gGeIsxzju6ZcgiyuJZT19zh0CSKZyVUk6PmU7wIwcH7r9lNLRJl061Ly6
oK9pQSQ48xhHFiRX8aW2tSrxLNiYDQ+pDhkshhH8pBAFZBWF6ynn2fAzBWyyPM24
V3pNrdXLCgM19eh8SgCgana1Q+QVEjvq6my6oj+eg3GLyQ4MA3cwGCy7IiFxdbJp
IpIxQ4548fLS6rX4kZxQ5g/XokxhKcNezDTgNfG0j46hV3KB9o3QMExcH6VFEx+7
vdNbh7vQtnuFnuoFc2CPAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQCp
MQEXuJEzZcsG03kZMeRiPebzJzlrLrmWe1bZ7RGcDoAmA/3mFWhsY3xIz71pL7X1
lk7u1VHjQ4g4KFPWeT7mUKHKNx3+a3P4uiCtixlHaoQDzLT/TGascJdnRPRs7DDx
Ti2Pws6TTU2TGQ8miOrufmOSLjC/cnOWugJ8N2PLfLc/qmTEmUSofzoSYYxMooa8
sMDqxTziIv3udUMAt56KVGtEJDMV4II/q317igfJfLvhYwfPDIcdKwV2MMYXELBS
uue1x9wArxc7dJLMp/CzuFsUCl9mYNwsaXufIAjH1wr7odAm39XPydYPJ9p/oTMP
Ni4diLNLwNYTdLz+zcZ1
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
    Session-ID: E4E9F0C8DA6FC8DD745D51B1CC62EDED27DFDDAF86ABCA771902444CDC456E37
    Session-ID-ctx:
    Resumption PSK: BEEFAAC83E1C926D03C7974F864245CCC94CA782A1914A74071DD3FE8414811729080A2523931AEEC37E7B9C03421C72
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - b5 91 1a 70 94 c3 f3 ac-89 ba 6c a2 69 28 4d 13   ...p......l.i(M.
    0010 - d4 39 73 9f 15 e7 ec 53-6a 8d 58 e4 98 b9 a4 29   .9s....Sj.X....)
    0020 - cf 88 c5 d1 8e 6a 77 ba-d2 3c 51 35 e7 82 d5 97   .....jw..<Q5....
    0030 - cd 7c f0 b1 8f 0e 52 86-e8 52 c0 dd 5e 57 00 2e   .|....R..R..^W..
    0040 - d4 eb ba 14 76 aa 1d 49-f2 2a a6 d2 28 01 e6 e5   ....v..I.*..(...
    0050 - 89 6c c3 c1 a1 15 dd 03-aa 16 40 80 d3 d1 89 e5   .l........@.....
    0060 - f9 6a 6f 23 40 b1 6a dc-c0 bb aa 53 5f 85 1d db   .jo#@.j....S_...
    0070 - 66 4a 80 c0 33 25 4c 8c-95 23 d2 70 76 54 c6 55   fJ..3%L..#.pvT.U
    0080 - 71 14 69 58 c1 cb 45 f1-26 94 5b 6d 34 bf 52 cf   q.iX..E.&.[m4.R.
    0090 - b3 ff e7 5d a1 9b 79 69-e4 9e 80 a6 86 4c 8a 40   ...]..yi.....L.@
    00a0 - 67 d3 93 44 6a b3 79 9c-32 76 07 e2 b2 f4 58 26   g..Dj.y.2v....X&
    00b0 - 42 cd 06 0d a4 c4 cb c3-0a b5 15 c7 49 89 4d 53   B...........I.MS
    00c0 - a7 b6 ef 95 d9 21 61 6c-ce 46 f1 cd 24 a0 02 b8   .....!al.F..$...

    Start Time: 1676575398
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
    Session-ID: 1B326870F874BB871AC58DBF264BF9F900AAD6F169CFE5DF6FEB4F97C9F0C8AC
    Session-ID-ctx:
    Resumption PSK: 4AC63137ED25DCDCFEC32E08F23A183EF5365CD085752B545A0675C7CE34DEA4606429F72FA5A78203DF793010527FE8
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - b5 91 1a 70 94 c3 f3 ac-89 ba 6c a2 69 28 4d 13   ...p......l.i(M.
    0010 - 0f c7 5a 66 27 12 3b 0a-1b f6 1f a9 f8 55 45 b1   ..Zf'.;......UE.
    0020 - 77 b9 9b 64 ca f7 35 e4-da dc 92 01 af e1 41 cd   w..d..5.......A.
    0030 - 2b 91 05 66 a3 bb c5 45-0b 4e 0a f9 5e 08 eb a5   +..f...E.N..^...
    0040 - 6e 98 79 0e 45 42 a1 27-4b d8 ed a3 25 2e d1 11   n.y.EB.'K...%...
    0050 - 08 ad 68 6d b0 84 10 70-d3 18 80 c5 5e 07 de 05   ..hm...p....^...
    0060 - 97 bf db ab d2 db 4c ad-2d 9a 13 dc 06 91 73 aa   ......L.-.....s.
    0070 - c9 29 46 4e 82 c4 3e 9b-a4 1f 8e 2b 1d 4b 26 2c   .)FN..>....+.K&,
    0080 - 55 7f 19 f9 b5 c3 77 be-02 2d dd 2a e7 83 e7 19   U.....w..-.*....
    0090 - df 33 b1 29 7a 1c 22 19-2e 4b 4a 9b c6 03 d5 eb   .3.)z."..KJ.....
    00a0 - 2d 30 fa fd 87 e1 0a 78-23 f8 8b c0 9e 24 6f 57   -0.....x#....$oW
    00b0 - cb 9f 5e 9b 85 f4 21 a1-9d 65 ab 14 0c ce f6 67   ..^...!..e.....g
    00c0 - 8c f0 d0 70 3b e8 99 9c-e4 a7 a7 51 29 3c bf 2e   ...p;......Q)<..

    Start Time: 1676575398
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
bandit15@bandit:~$
```
## Notas adicionales

#### Definiciones que entender
- **Certificados SSL/TLS de servidor web**: Estos certificados nos permitirán establecer comunicaciones con sus clientes utilizando la tecnología SSL o TLS, los estándares para comunicaciones seguras en la Web. Su servidor se identificará a los clientes con el nombre del dominio donde se encuentra su servicio Web, además de garantizar la integridad y confidencialidad de las comunicaciones.

#### Comandos Linux Utilizados 

- **openssl**: Comando que sirve para crear, convertir, gestionan los Certificados SSL, viene con una herramienta de cliente que puede usar para conectarse a un servidor seguro.

-  **s_client**: Comando en el cual implementa un cliente SSL/TLS genérico que se conecta a un host remoto mediante SSL/TLS. Es una herramienta de diagnóstico muy útil para servidores SSL.

- **-connect**: Comando y/o Interruptor que se usa para establecer la conexión TCP. 

## Referencias
- https://en.wikipedia.org/wiki/Transport_Layer_Security#SSL_1.0,_2.0,_and_3.0
- https://www.feistyduck.com/library/openssl-cookbook/online/
- https://www.cert.fnmt.es/componente/certificado-servidor
- https://www.openssl.org/docs/man1.1.1/man1/openssl-s_client.html#:~:text=The%20s_client%20command%20implements%20a,diagnostic%20tool%20for%20SSL%20servers.