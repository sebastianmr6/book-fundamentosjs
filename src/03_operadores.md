# Operadores en JavaScript
JavaScript ofrece una variedad de operadores que permiten realizar operaciones sobre valores y variables. A continuación, se describen los principales tipos de operadores:
## Operadores Aritméticos
Los operadores aritméticos se utilizan para realizar operaciones matemáticas básicas:
- `+` : Suma
```javascript
let a = 5;
let b = 3;
let suma = a + b; 
console.log(suma);
> 8
```
- `-` : Resta
```javascript
let a = 5;
let b = 3;
let resta = a - b; 
console.log(resta);
> 2
```
- `*` : Multiplicación
```javascript
let a = 5;
let b = 3;
let multiplicacion = a * b; 
console.log(multiplicacion);
> 15
```
- `/` : División
```javascript
let a = 6;
let b = 3;
let division = a / b;
console.log(division);
> 2
```
- `%` : Módulo (resto de una división)
```javascript
let a = 10;
let b = 4;
let modulo = a % b;
console.log(modulo);
> 2
```
- `++` : Incremento
```javascript
let a = 5;
a++;
console.log(a);
> 6
```
- `--` : Decremento
```javascript
let a = 5;
a--;
console.log(a);
> 4
```
## Operadores de Asignación
Los operadores de asignación se utilizan para asignar valores a las variables:
- `=` : Asignación simple
```javascript
let a = 10;
console.log(a);
> 10
```
- `+=` : Asignación con suma
```javascript
let numero = 5;
numero += 3; // Equivalente a numero = numero + 3
console.log(numero);
> 8
```
- `-=` : Asignación con resta
```javascript
let numero = 5;
numero -= 2; // Equivalente a numero = numero - 2
console.log(numero);
> 3
```
- `*=` : Asignación con multiplicación
```javascript
let numero = 5;
numero *= 4; // Equivalente a numero = numero * 4
console.log(numero);
> 20
```
- `/=` : Asignación con división
```javascript
let numero = 20;
numero /= 5; // Equivalente a numero = numero / 5
console.log(numero);
> 4
```
- `%=` : Asignación con módulo
```javascript
let numero = 10;
numero %= 3; // Equivalente a numero = numero % 3
console.log(numero);
> 1
```
## Operadores de Comparación
Los operadores de comparación se utilizan para comparar dos valores:
- `==` : Igualdad (compara valores)
```javascript
let a = 5;
let b = '5';
console.log(a == b);
> true
```
- `===` : Igualdad estricta (compara valores y tipos)
```javascript
let a = 5;
let b = '5';
console.log(a === b);
> false
```
- `!=` : Desigualdad (compara valores)
```javascript
let a = 5;
let b = '6';
console.log(a != b);
> true
```
- `!==` : Desigualdad estricta (compara valores y tipos)
- `>` : Mayor que
- `<` : Menor que
- `>=` : Mayor o igual que
- `<=` : Menor o igual que
## Operadores Lógicos
Los operadores lógicos se utilizan para combinar expresiones booleanas:
- `&&` : AND lógico
- `||` : OR lógico
- `!` : NOT lógico
## Operadores de Cadena
Los operadores de cadena se utilizan para manipular cadenas de texto:
- `+` : Concatenación de cadenas
- `+=` : Concatenación y asignación
## Operadores Ternarios
El operador ternario es una forma abreviada de una declaración `if-else`:
```javascript
condición ? expresión1 : expresión2
```
Si la condición es verdadera, se evalúa `expresión1`; de lo contrario, se evalúa `expresión2`.
## Operadores de Tipo
Los operadores de tipo se utilizan para obtener información sobre el tipo de dato de una variable:
- `typeof` : Devuelve una cadena que indica el tipo de dato
- `instanceof` : Comprueba si un objeto es una instancia de una clase específica
Estos operadores son fundamentales para la manipulación de datos y el control del flujo en JavaScript.
