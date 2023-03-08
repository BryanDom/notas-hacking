## Objetivo

Our flag printing service has started glitching!`$ nc saturn.picoctf.net 51109`

## Solución
```
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ nc saturn.picoctf.net 51109
'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3          
Python 3.10.8 (main, Nov  4 2022, 09:21:25) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print('picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}')
picoCTF{gl17ch_m3_n07_bda68f75}
>>> exit()
                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 

```

## Bandera

### `picoCTF{gl17ch_m3_n07_bda68f75}`
 
## Notas adicionales

#### Definiciones que entender

Cuando nos conectamos al dicho comando y puerto que se nos esta dando, nos esta dando la bandera "icompleta", ya que contiene caracteres ASCII, entonces se me ocurrio que *python* convierte esos caracteres ASCII en las letras correspondientes, esto fue ocurrido ya que lo investigue en fuentes para no complicarme en el desarrollo de codigo o algo por el estilo.

## Referencias

- https://micro.recursospython.com/recursos/como-obtener-el-codigo-ascii-de-un-caracter.html
- https://www.josedomingo.org/pledin/2017/02/codificacion-de-caracteres-en-python2/