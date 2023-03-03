## Objetivo

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file)? This would be really tedious to look through manually, something tells me there is a better way.

## Solución
```
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file              
--2023-03-03 13:16:03--  https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 14551 (14K) [application/octet-stream]
Saving to: ‘file’

file                                                       100%[=======================================================================================================================================>]  14.21K  --.-KB/s    in 0s      

2023-03-03 13:16:04 (219 MB/s) - ‘file’ saved [14551/14551]                                                  
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls
bandera  file                                                         
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ cat file | grep pico
picoCTF{grep_is_good_to_find_things_f77e0797}                                     
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 

```

### `picoCTF{grep_is_good_to_find_things_f77e0797}`

## Notas adicionales

#### Comandos Linux Utilizados 

- **wget**: Comando que nos permite la descarga de contenidos desde servidores web de una forma simple y rápida.

- **grep**: Comando que nos permite buscar una palabra o patron, e imprimir las líneas que la contienen, utilizada para buscar texto dentro de archivos.

#### Definiciones que entender

La cadena está codificada en base64, en este caso se puede utilizar un decodificador (lo utilice para verificar) o hacerlo manualmente en linux (como lo mostre).

## Referencias

-  https://docs.oracle.com/cd/E19620-01/805-7644/6j76klop3/index.html
- https://www.hostinger.mx/tutoriales/usar-comando-wget/#:~:text=descargar%20archivos%20numerados-,%C2%BFQu%C3%A9%20es%20el%20Comando%20Wget%3F,Web%20y%20la%20palabra%20get.