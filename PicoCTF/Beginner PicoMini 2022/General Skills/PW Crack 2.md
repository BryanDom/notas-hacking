## Objetivo

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/18/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level2.flag.txt.enc) in the same directory too.

## Solución
```
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://artifacts.picoctf.net/c/18/level2.py          
--2023-03-08 16:44:55--  https://artifacts.picoctf.net/c/18/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.21.66, 13.249.21.32, 13.249.21.46, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.21.66|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: ‘level2.py’

level2.py           100%[================>]     914  --.-KB/s    in 0s      

2023-03-08 16:44:55 (8.67 MB/s) - ‘level2.py’ saved [914/914]

                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://artifacts.picoctf.net/c/18/level2.flag.txt.enc
--2023-03-08 16:45:05--  https://artifacts.picoctf.net/c/18/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.21.66, 13.249.21.46, 13.249.21.85, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.21.66|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: ‘level2.flag.txt.enc’

level2.flag.txt.enc 100%[================>]      31  --.-KB/s    in 0s      

2023-03-08 16:45:06 (14.3 MB/s) - ‘level2.flag.txt.enc’ saved [31/31]

                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls
codebook.txt  fixme1.py            level1.py            runme.py
code.py       fixme2.py            level2.flag.txt.enc
convertme.py  level1.flag.txt.enc  level2.py
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 level2.py
Please enter correct password for flag: ^Z
zsh: suspended  python3 level2.py
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ nano level2.py
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python           
Python 3.10.8 (main, Nov  4 2022, 09:21:25) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65))
39ce
>>> exit()
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 level2.py
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 

```

## Bandera

### `picoCTF{tr45h_51ng1ng_502ec42e}`
 
## Notas adicionales

#### Definiciones que entender

Simplemente me pedia una contraseña para corre el programa de python que se descargo, en este caso se me daba otro documenta donde *creo* estaba la contraseña, no sabía que hacer con el o como descifrar dicho texto, haci que se me ocurrio revisar el codigo haber si tenia la contraseña en alguna linea de codigo y "si" lo tenía, pero lo tenia como *chr*, asi que este reto era igual como uno antes que habia resuelto, solamente corrí python le di *print* y puse la siguiente cadena: *chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65)* y la contraseña fue *39ce* y fue todo, el siguiente codigo fue donde encontre dicha cadena:

```
def level_2_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")
```
## Referencias