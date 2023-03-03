## Objetivo

Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm) has extraordinarily helpful information...
## Solución
```
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm
--2023-03-03 13:57:35--  https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: ‘warm’

warm                                                       100%[=======================================================================================================================================>]  10.68K  --.-KB/s    in 0s      

2023-03-03 13:57:35 (264 MB/s) - ‘warm’ saved [10936/10936]                                                     
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls
bandera  file  flag  warm                                                     
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls -l
total 792
-rw-r--r-- 1 kali kali 776032 Oct 26  2020 bandera
-rw-r--r-- 1 kali kali  14551 Oct 26  2020 file
-rw-r--r-- 1 kali kali     34 Mar 16  2021 flag
-rw-r--r-- 1 kali kali  10936 Mar 15  2021 warm                                                  
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ chmod 777 warm                                                    
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_18788aaa}                                           
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 

```

### `picoCTF{b1scu1ts_4nd_gr4vy_18788aaa}  `

## Notas adicionales

#### Comandos Linux Utilizados 

- **chmod 777**: Este comando indica que se está cambiando el modo en que se puede acceder al archivo o directorio. "777" es un conjunto de permisos que se están aplicando al archivo o directorio "warm".

- **-h**: argumento o opción que se le está pasando al archivo "warm", que generalmente se utiliza para solicitar información de ayuda o mostrar la sintaxis correcta de uso del programa.

En particular, estos permisos significan lo siguiente:

-   El primer dígito "7" indica que el propietario del archivo (el usuario que lo creó) tiene permisos de lectura, escritura y ejecución (rwx).
-   El segundo dígito "7" indica que los usuarios del mismo grupo que el propietario tienen permisos de lectura, escritura y ejecución (rwx).
-   El tercer dígito "7" indica que los usuarios que no son el propietario ni pertenecen al mismo grupo tienen permisos de lectura, escritura y ejecución (rwx).

## Referencias

-  https://es.wikipedia.org/wiki/Chmod#:~:text=chmod%2C%20que%20significa%20%22cambiar%20modo,a%20carpetas%20o%20directorios%E2%80%8B.