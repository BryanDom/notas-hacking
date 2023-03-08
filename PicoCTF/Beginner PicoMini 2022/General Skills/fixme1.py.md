## Objetivo

Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/39/fixme1.py)

## Solución
```                                                              
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://artifacts.picoctf.net/c/39/fixme1.py    
--2023-03-08 16:06:59--  https://artifacts.picoctf.net/c/39/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.21.85, 13.249.21.46, 13.249.21.32, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.21.85|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: ‘fixme1.py’

fixme1.py           100%[================>]     837  --.-KB/s    in 0s      

2023-03-08 16:07:00 (8.03 MB/s) - ‘fixme1.py’ saved [837/837]

                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls
codebook.txt  code.py  convertme.py  fixme1.py  runme.py
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 fixme1.py
  File "/home/kali/Documents/PicoCTF/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
                                                                             
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ nano fixme1.py
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 

```
## Bandera

### `picoCTF{1nd3nt1ty_cr1515_182342f7}`
 
## Notas adicionales

#### Definiciones que entender
Como se dice en el programa al momento de correrlo, esta mal intentado una linea de codigo, en el cual esta en la ultima:

```
flag = str_xor(flag_enc, 'enkidu')
	print('That is correct! Here\'s your flag: ' + flag)
```

en el cual solamente hice esto:
```
flag = str_xor(flag_enc, 'enkidu')
print('That is correct! Here\'s your flag: ' + flag)
```

 y es todo, solamente entre con el comando *nano* para corregir dicha linea.
 
## Referencias