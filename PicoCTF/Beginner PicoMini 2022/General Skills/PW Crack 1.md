## Objetivo

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/52/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/52/level1.flag.txt.enc) in the same directory too.

## Solución
```
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls
codebook.txt  convertme.py  fixme2.py            level1.py
code.py       fixme1.py     level1.flag.txt.enc  runme.py
                                                                             
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 level1.py
Please enter correct password for flag: ^Z
zsh: suspended  python3 level1.py
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ cat level1.flag.txt.enc
A
 Rr1w▒Q nVT_nPRVW▒                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ nano level1.py
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 level1.py
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 

```
## Bandera

### `picoCTF{545h_r1ng1ng_fa343060}`
 
## Notas adicionales

#### Definiciones que entender

Simplemente me pedia una contraseña para corre el programa de python que se descargo, en este caso se me daba otro documenta donde *creo* estaba la contraseña, no sabía que hacer con el o como descifrar dicho texto, haci que se me ocurrio revisar el codigo haber si tenia la contraseña en alguna linea de codigo y "si" lo tenía, a continuación muestro donde lo encontre y dicha contraseña fue *1e1a*.

```
def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "1e1a"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
```
## Referencias