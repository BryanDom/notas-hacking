## Objetivo

Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](https://artifacts.picoctf.net/c/86/runme.py)

## Solución
```
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://artifacts.picoctf.net/c/86/runme.py
--2023-03-08 15:54:43--  https://artifacts.picoctf.net/c/86/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.22, 13.249.74.17, 13.249.74.69, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.22|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: ‘runme.py’

runme.py            100%[================>]     270  --.-KB/s    in 0s      

2023-03-08 15:54:43 (119 MB/s) - ‘runme.py’ saved [270/270]

                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls
runme.py
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 runme.py
picoCTF{run_s4n1ty_run}
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 

```
## Bandera

### `picoCTF{run_s4n1ty_run}`
 
## Notas adicionales

#### Definiciones que entender

- El reto solamente consistia en correr el archivo python que descargamos desde una terminal linux, y asi nos daba la "bandera".

## Referencias