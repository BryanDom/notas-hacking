## Objetivo

Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 14291`.

## Solución
```
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ nc jupiter.challenges.picoctf.org 14291 | grep pico
picoCTF{digital_plumb3r_ea8bfec7}                                                 
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 

```

### `picoCTF{digital_plumb3r_ea8bfec7}`

## Notas adicionales

#### Comandos Linux Utilizados 

- **nc**: s una utilidad utilizada en Linux y otros sistemas operativos similares a Unix para leer, escribir y transmitir datos a través de una red. A menudo se usa para probar conexiones de red, escanear puertos y transferir archivos entre sistemas..
- **grep**: Comando que nos permite buscar una palabra o patron, e imprimir las líneas que la contienen, utilizada para buscar texto dentro de archivos.

#### Definiciones que entender

Al momento que nos conectamos a este puerto, nos reciben muchas líneas de mensajes de relleno. En este caso podemos usar una pipa |. Lo que hace una tubería en Shell es que nos permite combinar dos comandos en uno. Entonces, si quisiéramos grep el valor de retorno de la conexión del host netcat para un indicador, podemos ejecutar como en la solución para obtener la bandera

## Referencias

- http://linfo.org/pipes.html