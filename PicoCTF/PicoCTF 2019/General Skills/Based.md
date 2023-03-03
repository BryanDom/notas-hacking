## Objetivo

To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 15130`.

## Solución
```
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ nc jupiter.challenges.picoctf.org 15130
Let us see how data is stored
test
Please give the 01110100 01100101 01110011 01110100 as a word.
...
you have 45 seconds.....

Input:
test
Please give me the  156 165 162 163 145 as a word.
Input:
nurse
Please give me the 737472656574 as a word.
Input:
street
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_02167de8}                                                 
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 
```

### `picoCTF{learning_about_converting_values_02167de8}`

## Notas adicionales

#### Comandos Linux Utilizados 

- **nc**: s una utilidad utilizada en Linux y otros sistemas operativos similares a Unix para leer, escribir y transmitir datos a través de una red. A menudo se usa para probar conexiones de red, escanear puertos y transferir archivos entre sistemas..

#### Definiciones que entender

El reto consistía en desifrar lo que se me pedia, esto con ayuda de aplicaciones que estan en internet.

## Referencias

-  https://ccia.esei.uvigo.es/docencia/SCS/1011/practicas/practica-1/index.html#:~:text=interfaz%20de%20SOCKETS.-,Comando%20nc%2Fnetcat,UDP)%20de%20la%20m%C3%A1quina%20local.
- https://www.traductorbinario.com/
- https://elcodigoascii.com.ar/