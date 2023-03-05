## Objetivo

Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/static)? This [BASH script](https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/ltdis.sh) might help!

## Solución
```                                               
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/ltdis.sh
--2023-03-05 12:22:46--  https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/ltdis.sh
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: ‘ltdis.sh’

ltdis.sh                                                   100%[=======================================================================================================================================>]     785  --.-KB/s    in 0s      

2023-03-05 12:22:47 (2.40 MB/s) - ‘ltdis.sh’ saved [785/785]
                                                   
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/static  
--2023-03-05 12:23:00--  https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
Saving to: ‘static’

static                                                     100%[=======================================================================================================================================>]   8.18K  --.-KB/s    in 0s      

2023-03-05 12:23:00 (138 MB/s) - ‘static’ saved [8376/8376]
                                                        
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls
bandera  convertidor.py  convertir-numeros  file  flag  ltdis.sh  static  warm
                                                       
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ./ltdis.sh static 
zsh: permission denied: ./ltdis.sh
                                                    
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ chmod 777 ltdis.sh 
                                                       
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ./ltdis.sh static 
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
                                                                                                                                   
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls
bandera  convertidor.py  convertir-numeros  file  flag  ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt  warm
                                                        
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ cat static.ltdis.strings.txt | grep pico
   1020 picoCTF{d15a5m_t34s3r_ccb2b43e}
                                                  
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 

```

### `picoCTF{d15a5m_t34s3r_ccb2b43e}`

## Notas adicionales

#### Comandos Linux Utilizados 

- **chmod 777**: Este comando indica que se está cambiando el modo en que se puede acceder al archivo o directorio. "777" es un conjunto de permisos que se están aplicando al archivo o directorio "ltdis.sh" ya que no tenemos permiso.

En particular, estos permisos significan lo siguiente:

-   El primer dígito "7" indica que el propietario del archivo (el usuario que lo creó) tiene permisos de lectura, escritura y ejecución (rwx).
-   El segundo dígito "7" indica que los usuarios del mismo grupo que el propietario tienen permisos de lectura, escritura y ejecución (rwx).
-   El tercer dígito "7" indica que los usuarios que no son el propietario ni pertenecen al mismo grupo tienen permisos de lectura, escritura y ejecución (rwx).

#### Definiciones que entender

**./ltdis.sh static**: El script "ltdis.sh" está desensamblado (disassembling) un archivo binario llamado "static" y extrayendo cadenas de texto del mismo, es decir, el script "ltdis.sh" está realizando análisis de ingeniería inversa (reverse engineering) en el archivo binario "static" y extrayendo información útil del mismo.

En el cual en el desensamblado La salida indica que se ha creado un archivo de texto llamado "static.ltdis.x86_64.txt" que contiene el código desensamblado del archivo "static".

Además, el script también está extrayendo cadenas de texto del archivo binario y escribiéndolas en otro archivo de texto llamado "static.ltdis.strings.txt", junto con su desplazamiento de archivo, en el cual contiene dicha bandera del reto.

## Referencias

- https://www.hostinger.mx/tutoriales/cambiar-permisos-y-propietarios-linux-linea-de-comandos/
- https://docs.oracle.com/cd/E19620-01/805-7644/6j76klop3/index.html#:~:text=grep%20se%20utiliza%20muy%20a,de%20comunicaci%C3%B3n%20es%20%22%20%7C%20%22.
-  https://www.howtogeek.com/427805/how-to-use-the-strings-command-on-linux/