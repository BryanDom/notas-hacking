## Objetivo

This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/fb851c1858cc762bd4eed569013d7f00/flag).
## Solución
```
                                                                                                                                                                                                                                          
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://mercury.picoctf.net/static/fb851c1858cc762bd4eed569013d7f00/flag
--2023-03-03 13:55:27--  https://mercury.picoctf.net/static/fb851c1858cc762bd4eed569013d7f00/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: ‘flag’

flag                                                       100%[=======================================================================================================================================>]      34  --.-KB/s    in 0s      

2023-03-03 13:55:27 (44.2 MB/s) - ‘flag’ saved [34/34]                                                      
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls
bandera  file  flag                                                  
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ cat flag
picoCTF{s4n1ty_v3r1f13d_28e8376d}                                                 
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 


```

### `picoCTF{s4n1ty_v3r1f13d_28e8376d}`

## Notas adicionales

#### Comandos Linux Utilizados 

- **wget**: Comando que nos permite la descarga de contenidos desde servidores web de una forma simple y rápida.

## Referencias

-  https://geekflare.com/es/wget-command-examples/