## Objetivo

There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 22902`, but it doesn't speak English...

## Solución
```
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ nc mercury.picoctf.net 22902 | tr '\n' ' ' >  convertir-numeros 
                                                  
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ cat convertir-numeros
112  105  99  111  67  84  70  123  103  48  48  100  95  107  49  116  116  121  33  95  110  49  99  51  95  107  49  116  116  121  33  95  100  51  100  102  100  54  100  102  125  10                                                                                                                                                                                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ nano convertidor.py                                                                                             
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ cat convertidor.py   
linea = input().split()

for i in linea:
        digito = int(i)
        print(chr(digito), end="")

print("")                                                    
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 convertidor.py < convertir/numeros 
zsh: no such file or directory: convertir/numeros                                                   
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ python3 convertidor.py < convertir-numeros 
picoCTF{g00d_k1tty!_n1c3_k1tty!_d3dfd6df}                                                    
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ 

```

### `picoCTF{g00d_k1tty!_n1c3_k1tty!_d3dfd6df}`

## Notas adicionales

#### Comandos Linux Utilizados 

- **tr**: Comando en el cual se utiliza para traducir o borrar caracteres en un archivo o entrada de texto, en el cual en este caso substituimos los saltos de linea por espacios guardandolo en un archivo.

- **nano**: Comando en el cual se utiliza principalmente para editar archivos de configuración del sistema y scripts de shell en la terminal de Linux, en el cual lo usamos para poner el codigo respectivo de python.

#### Definiciones que entender

Tambien verifique en un programa para validar que fuera correcto el convertidor que cree en python.

## Referencias

-  https://gchq.github.io/CyberChef/#recipe=From_Decimal('Line%20feed',false).
- https://geekland.eu/uso-del-comando-tr-en-linux-y-unix-con-ejemplos/
- https://adclichosting.com/knowledgebase/comandos-del-editor-nano/