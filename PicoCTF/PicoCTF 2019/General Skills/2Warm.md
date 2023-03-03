## Objetivo

Can you convert the number 42 (base 10) to binary (base 2)?

## Solución

### `picoCTF{101010}`
 
## Notas adicionales

#### Definiciones que entender
Para convertir el numero 42 (base 10) a binario, necesitamos dividir el número decimal repetidamente por 2 y registrar el resto de cada división. Continuamos este proceso hasta que el cociente sea 0.

Apliquemos este proceso al número que mencionamos:

-   Divide 42 entre 2. El cociente es 21 y el resto es 0.
-   Divide 21 entre 2. El cociente es 10 y el resto es 1.
-   Divide 10 entre 2. El cociente es 5 y el resto es 0.
-   Divide 5 entre 2. El cociente es 2 y el resto es 1.
-   Divide 2 entre 2. El cociente es 1 y el resto es 0.
-   Divide 1 entre 2. El cociente es 0 y el resto es 1.

Ahora, anotamos los residuos en orden inverso, comenzando desde abajo:

42 decimal = 101010 binario

Por lo tanto, la representación binaria de 42 es 101010.
## Referencias

- https://www.cuemath.com/numbers/42-in-binary/
- https://wims.univ-cotedazur.fr/wims/en_tool~number~baseconv.en.html