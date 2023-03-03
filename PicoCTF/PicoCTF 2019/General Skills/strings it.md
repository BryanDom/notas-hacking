## Objetivo

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings) without running it?

## Solución
```
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings
--2023-03-02 23:23:22--  https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: ‘strings’

strings                                                    100%[=======================================================================================================================================>] 757.84K  1.92MB/s    in 0.4s    

2023-03-02 23:23:23 (1.92 MB/s) - ‘strings’ saved [776032/776032]
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls   
strings
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ mv strings bandera                                                                    
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls
bandera
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ strings bandera | grep pico      
picoCTF{5tRIng5_1T_d66c7bb7}
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 

```

### `picoCTF{5tRIng5_1T_d66c7bb7}`


## Notas adicionales

#### Comandos Linux Utilizados 

- **wget**: Comando que nos permite la descarga de contenidos desde servidores web de una forma simple y rápida.

- **strings**: Comando que nos permite obtener los caracteres legibles de un archivo binario no legible, es decir, utilizada para extraer cadenas de texto imprimibles de archivos binarios.

- **grep**: Comando que nos permite buscar una palabra o patron, e imprimir las líneas que la contienen, utilizada para buscar texto dentro de archivos.

## Referencias

- https://www.hostinger.mx/tutoriales/usar-comando-wget/#:~:text=descargar%20archivos%20numerados-,%C2%BFQu%C3%A9%20es%20el%20Comando%20Wget%3F,Web%20y%20la%20palabra%20get.
- https://francisconi.org/linux/comandos/strings
- https://docs.oracle.com/cd/E19620-01/805-7644/6j76klop3/index.html