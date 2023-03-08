## Objetivo

Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/31/convertme.py)

## Solución

```  
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://artifacts.picoctf.net/c/31/convertme.py
--2023-03-08 15:56:52--  https://artifacts.picoctf.net/c/31/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.21.46, 13.249.21.85, 13.249.21.32, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.21.46|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: ‘convertme.py’

convertme.py        100%[================>]   1.16K  --.-KB/s    in 0s      

2023-03-08 15:56:52 (12.3 MB/s) - ‘convertme.py’ saved [1189/1189]

                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls
convertme.py  runme.py
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 convertme.py
If 94 is in decimal base, what is it in binary base?
Answer: 1011110
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_9c3b7d4d}
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 


```
## Bandera

### `picoCTF{4ll_y0ur_b4535_9c3b7d4d}`
 
## Notas adicionales

#### Definiciones que entender

Para convertir este número a la base binaria, se puede utilizar el método de división sucesiva. El proceso es el siguiente:

1.  Dividir 94 entre 2, y anotar el cociente y el residuo:
    -   Cociente: 47
    -   Residuo: 0
2.  Dividir el cociente anterior (47) entre 2, y anotar el cociente y el residuo:
    -   Cociente: 23
    -   Residuo: 1
3.  Dividir el nuevo cociente (23) entre 2, y anotar el cociente y el residuo:
    -   Cociente: 11
    -   Residuo: 1
4.  Dividir el nuevo cociente (11) entre 2, y anotar el cociente y el residuo:
    -   Cociente: 5
    -   Residuo: 1
5.  Dividir el nuevo cociente (5) entre 2, y anotar el cociente y el residuo:
    -   Cociente: 2
    -   Residuo: 1
6.  Dividir el nuevo cociente (2) entre 2, y anotar el cociente y el residuo:
    -   Cociente: 1
    -   Residuo: 0
7.  Dividir el último cociente (1) entre 2, y anotar el cociente y el residuo:
    -   Cociente: 0
    -   Residuo: 1

Ahora, para obtener la representación binaria de 94, se deben leer los residuos de abajo hacia arriba, de modo que la respuesta es:

94 en base binaria = 1011110

- Tambien lo comprobe en una página para ver si estaba correcto.

## Referencias

- https://es.convertbinary.com/decimal-a-binario/
- http://platea.pntic.mec.es/~lgonzale/tic/binarios/numeracion.html#:~:text=El%20sistema%20de%20numeraci%C3%B3n%20binario,posici%C3%B3n%20del%20d%C3%ADgito%20menos%20uno.