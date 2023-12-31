# Minerva
Autómata finito determinista que permite reconocer y validar si una cadena de caracteres, conformada por los símbolos del alfabeto de la numeración romana, corresponde o no con un número romano escrito correctamente.

- [x] Puede reconocer y validar números del 1 al 3999.
- [x] Si se ingresa en el estado rechazador se deja de procesar automáticamente.

### Características de la numeración romana
- Los caracteres se leen de izquierda a derecha.
- Un símbolo que es seguido de otro igual o menor conforma una suma.
- Un símbolo seguido de otro mayor forma un subconjunto donde el menor se resta del mayor.
- Los símbolos de base 5 (V, L, D) no pueden repetirse seguidos.
- Los símbolos de base 10 (I, X, C, M) pueden repetirse hasta 3 veces sumando.
- Los símbolos de base 5 (V, L, D) no pueden usarse para restar.
- Los símbolos de base 10 (I, X, C, M) pueden restar siguiendo dos reglas:
	- A números de base 5 y 10 inmediatamente superiores.
		
		| IV | IX | XL | XC | CD | CM |
		| :---: | :---: | :---: | :---: | :---: | :---: |
		| 4 | 9 | 40 | 90 | 400 | 900 |
		
	- Si están restando no pueden repetirse.
		
		| IV | IIV |
		| :---: | :---: |
		| 4 | - |
		| Bien | Mal |

### Mejoras posibles
- [ ] Retornar en sistema decimal el numero romano ingresado.
- [ ] Ampliar las reglas lógicas del autómata para reconocer números mayores a 3999 (MMMCMXCIX).

### Aplicación Web
La aplicación web se encuentra disponible en [**GitHub Pages**](https://augfer.github.io/Minerva/).
