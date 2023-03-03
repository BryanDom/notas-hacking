## Objetivo

What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.

## Solución
```
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ echo "bDNhcm5fdGgzX3IwcDM1" | base64 -d
l3arn_th3_r0p35                                                                                                                                                                                                                                           
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 
```

### `picoCTF{l3arn_th3_r0p35}`


## Notas adicionales

#### Comandos Linux Utilizados 

- **echo**: Utilidad de línea de comandos que se utiliza para imprimir un texto o una cadena de caracteres en la pantalla del terminal.

- **base64 -d**: se utiliza para decodificar datos en formato Base64.

#### Definiciones que entender

La cadena está codificada en base64, en este caso se puede utilizar un decodificador (lo utilice para verificar) o hacerlo manualmente en linux (como lo mostre).

## Referencias

- https://www.base64decode.org/
- https://ubunlog.com/base64-codificacion-decodificacion-terminal/
- https://codebeautify.org/base64-decode