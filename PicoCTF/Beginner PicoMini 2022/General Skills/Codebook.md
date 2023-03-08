## Objetivo

Run the Python script `code.py` in the same directory as `codebook.txt`.

-   [Download code.py](https://artifacts.picoctf.net/c/102/code.py)
-   [Download codebook.txt](https://artifacts.picoctf.net/c/102/codebook.txt)

## Solución
```                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://artifacts.picoctf.net/c/102/code.py    
--2023-03-08 16:02:52--  https://artifacts.picoctf.net/c/102/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.21.85, 13.249.21.46, 13.249.21.32, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.21.85|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: ‘code.py’

code.py             100%[================>]   1.25K  --.-KB/s    in 0s      

2023-03-08 16:02:52 (11.5 MB/s) - ‘code.py’ saved [1278/1278]

                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://artifacts.picoctf.net/c/102/codebook.txt
--2023-03-08 16:03:04--  https://artifacts.picoctf.net/c/102/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.21.85, 13.249.21.66, 13.249.21.46, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.21.85|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: ‘codebook.txt’

codebook.txt        100%[================>]      27  --.-KB/s    in 0s      

2023-03-08 16:03:05 (13.2 MB/s) - ‘codebook.txt’ saved [27/27]

                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls
codebook.txt  code.py  convertme.py  runme.py
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ cat codebook.txt
azbycxdwevfugthsirjqkplomn
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 code.py     
picoCTF{c0d3b00k_455157_197a982c}
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 

```  

## Bandera

### `picoCTF{c0d3b00k_455157_197a982c}`
 
## Notas adicionales

#### Definiciones que entender

Solamente hice "run" al programa de python, pero dicho programa lo necesitaba para correrlo (puede ser que lo llame dentro de su codigo) y es por eso que deben de estar juntos en un mismo directorio. 

## Referencias

- https://programacion.net/articulo/operaciones_con_ficheros_y_directorios_utilizando_python_1461