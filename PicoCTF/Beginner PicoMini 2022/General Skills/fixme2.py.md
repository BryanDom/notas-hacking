## Objetivo

Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/65/fixme2.py)

## Solución
```
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://artifacts.picoctf.net/c/65/fixme2.py
--2023-03-08 16:13:40--  https://artifacts.picoctf.net/c/65/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.21.46, 13.249.21.32, 13.249.21.66, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.21.46|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: ‘fixme2.py’

fixme2.py           100%[================>]   1.00K  --.-KB/s    in 0s      

2023-03-08 16:13:40 (10.5 MB/s) - ‘fixme2.py’ saved [1029/1029]

                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls
codebook.txt  code.py  convertme.py  fixme1.py  fixme2.py  runme.py
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 fixme2.py
  File "/home/kali/Documents/PicoCTF/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ nano fixme2.py
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 

```

## Bandera

### `picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}`
 
## Notas adicionales

#### Definiciones que entender
Como se dice en el programa al momento de correrlo, esta mal la sintaxis de una codicional del codigo, en el cual es esta:

```
if flag = "":
  print('String XOR encountered a problem, quitting.')
```

pero el error fue que le falto doble "=" asi que solamente le puse "= =" y fue todo para que funcionara adecuadamente:

```
if flag == "":
  print('String XOR encountered a problem, quitting.')
```

Para cambiar ese error, fue ingresando con el comando *nano*.
## Referencias
