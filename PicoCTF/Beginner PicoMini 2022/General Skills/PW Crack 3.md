## Objetivo

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/23/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/23/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/23/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

## Solución

  ```                                                                           
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://artifacts.picoctf.net/c/23/level3.py          
--2023-03-08 16:56:29--  https://artifacts.picoctf.net/c/23/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 54.230.253.65, 54.230.253.20, 54.230.253.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|54.230.253.65|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: ‘level3.py’

level3.py           100%[================>]   1.31K  --.-KB/s    in 0s      

2023-03-08 16:56:29 (12.3 MB/s) - ‘level3.py’ saved [1337/1337]

                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://artifacts.picoctf.net/c/23/level3.flag.txt.enc
--2023-03-08 16:56:39--  https://artifacts.picoctf.net/c/23/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.21.66, 13.249.21.32, 13.249.21.85, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.21.66|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: ‘level3.flag.txt.enc’

level3.flag.txt.enc 100%[================>]      31  --.-KB/s    in 0s      

2023-03-08 16:56:40 (532 KB/s) - ‘level3.flag.txt.enc’ saved [31/31]

                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://artifacts.picoctf.net/c/23/level3.hash.bin    
--2023-03-08 16:56:52--  https://artifacts.picoctf.net/c/23/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.21.66, 13.249.21.32, 13.249.21.85, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.21.66|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: ‘level3.hash.bin’

level3.hash.bin     100%[================>]      16  --.-KB/s    in 0s      

2023-03-08 16:56:53 (6.76 MB/s) - ‘level3.hash.bin’ saved [16/16]

                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls               
codebook.txt  fixme2.py            level2.py            runme.py
code.py       level1.flag.txt.enc  level3.flag.txt.enc
convertme.py  level1.py            level3.hash.bin
fixme1.py     level2.flag.txt.enc  level3.py
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 level3.py
Please enter correct password for flag: ^Z
zsh: suspended  python3 level3.py
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ nano level3.py
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ echo "6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e" 
6997, 3ac8, f0ac, 4b17, ec27, 4e66, 865e
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 level3.py
Please enter correct password for flag: 6997
That password is incorrect
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 level3.py
Please enter correct password for flag: 3ac8
That password is incorrect
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 level3.py
Please enter correct password for flag: f0ac
That password is incorrect
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 level3.py
Please enter correct password for flag: 4b17
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_2b072a90}
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 

```
## Bandera

### `picoCTF{m45h_fl1ng1ng_2b072a90}`
 
## Notas adicionales

#### Definiciones que entender

Simplemente en este reto me pedia una contraseña para corre el programa de python que se descargo, en este caso se me daba otro documenta donde *creo* estaba la contraseña, no sabía que hacer con el o como descifrar dicho texto, haci que se me ocurrio revisar el codigo haber si tenia la contraseña (como los casos contrarios) en alguna linea de codigo y "si" lo tenía, pero era una lista con las contraseñas y *era* nomas una de ellas, asi que lo que hice fue lo *tradicional* probar una por una y si le atine, la que fue la correcta fue *4b17*, y la lista de las contraseñas fue sacada del programa .py y fueron las siguientes:

```
pos_pw_list = ["6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e"]
```

## Referencias