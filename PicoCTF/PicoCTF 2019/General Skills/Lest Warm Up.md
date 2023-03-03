
## Objetivo

If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

## Solución

picoCTF{p}

## Notas adicionales

#### Definiciones que entender
0X70 es un número hexadecimal (hex). Podemos decir que es un número hexadecimal porque comienza con 0X

El sistema numérico hexadecimal tiene 16 símbolos (base 16) en lugar del sistema decimal que tiene 10 números (base 10). Los símbolos hexadecimales son 0 1 2 3 4 5 6 7 8 9 ABCDEF donde A=10, B=11, C=12. D=13, E=14 y F=15.

Convertir manualmente

Paso 1) Multiplica el último dígito por 1, Multiplica el penúltimo dígito por 16, Multiplica el tercero al último dígito por 16 x 16, Multiplique el cuarto al último dígito por 16 x 16 x 16, Multiplique el quinto al último dígito por 16 x 16 x 16 x 16 y así sucesivamente hasta usar todos los dígitos.

Paso 2) Sume todos los productos que obtuvo del Paso 1 para obtener la respuesta a 0X70 en decimal.

Aquí están las matemáticas utilizando los pasos anteriores que le muestran cómo convertir 0X70 a decimal.

0 x 1 = 0  
7 x 16 = 112

0 + 112 = 112

Valor 112 ascii = p

## Referencias

- http://www.asciichars.com/ascii-code-112
- https://elcodigoascii.com.ar/
- https://www.hexadecimaldictionary.com/hexadecimal/0x70/
- https://decimaltobinary.pro/_hexadecimal__70_in_decimal_-%7C-Work%2C-solution
- https://decimal.info/hex-to-decimal/7/how-to-convert-0X70-to-decimal.html