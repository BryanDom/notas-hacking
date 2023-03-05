## Objetivo

Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip)

## Solución
```                                               
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ wget https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip
--2023-03-05 12:42:31--  https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4520 (4.4K) [application/octet-stream]
Saving to: ‘Addadshashanammu.zip’

Addadshashanammu.zip                                       100%[=======================================================================================================================================>]   4.41K  --.-KB/s    in 0s      

2023-03-05 12:42:32 (8.22 No error) - ‘Addadshashanammu.zip’ saved [4520/4520]

                                                     
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls
Addadshashanammu.zip  bandera  convertidor.py  convertir-numeros  file  flag  ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt  warm
                                                                                                                                                 
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ unzip Addadshashanammu.zip
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
                                                        
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls
Addadshashanammu  Addadshashanammu.zip  bandera  convertidor.py  convertir-numeros  file  flag  ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt  warm
                                                                                                                                                
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls Addadshashanammu
Almurbalarammi
                                                                                                                                                
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ ls -R Addadshashanammu
Addadshashanammu:
Almurbalarammi

Addadshashanammu/Almurbalarammi:
Ashalmimilkala

Addadshashanammu/Almurbalarammi/Ashalmimilkala:
Assurnabitashpi

Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi:
Maelkashishi

Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi:
Onnissiralis

Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis:
Ularradallaku

Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku:
fang-of-haynekhtnamet
                                                                                                                                               
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ strings  Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet | grep pico
strings: 'Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet': No such file
                                                                                                                                               
┌──(kali㉿Brayan)-[~/Documents/PicoCTF]
└─$ cd Addadshashanammu 
                                                                                                                                            
┌──(kali㉿Brayan)-[~/Documents/PicoCTF/Addadshashanammu]
└─$ strings  Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet | grep pico
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_d32e018c}
                                                                                                                                        
┌──(kali㉿Brayan)-[~/Documents/PicoCTF/Addadshashanammu]
└─$ 

```

### `picoCTF{l3v3l_up!_t4k3_4_r35t!_d32e018c}`

## Notas adicionales

#### Comandos Linux Utilizados 

- **ls -R**: Este comando se utiliza para listar el contenido de un directorio y de sus subdirectorios de forma recursiva.
- **unzip**: Este comando se utiliza para descomprimir archivos ZIP y extraer su contenido en el sistema de archivos.
- **strings**: se utiliza para mostrar las cadenas de texto imprimibles en un archivo binario.

## Referencias

- https://respontodo.com/como-usar-el-comando-strings-en-linux/
- https://www.hostgator.mx/blog/principales-caracteristicas-de-unzip-linux/