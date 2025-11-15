# ¿Qué son los tipos de datos en JavaScript?
Los tipos de datos en JavaScript son las diferentes categorías de valores que pueden ser almacenados y manipulados en un programa. JavaScript es un lenguaje de tipado dinámico, lo que significa que no es necesario declarar el tipo de dato de una variable al momento de su creación; el tipo se determina automáticamente en tiempo de ejecución según el valor asignado. Es decir, una variable puede contener diferentes tipos de datos en diferentes momentos durante la ejecución del programa.

## Tipos de datos primitivos
Los tipos de datos primitivos en JavaScript son los siguientes:
- **String**: Representa secuencias de caracteres. Se pueden definir usando comillas simples, dobles o backticks. Ejemplo: `'Hola'`, `"Mundo"`, `` `Hola Mundo` ``.
- **Number**: Representa tanto números enteros como números de punto flotante. Ejemplo: `42`, `3.14`.
- **Boolean**: Representa valores lógicos, que pueden ser `true` (verdadero) o `false` (falso).
- **Null**: Representa la ausencia intencional de cualquier valor. Su valor es `null`.
- **Undefined**: Representa una variable que ha sido declarada pero no inicializada. Su valor es `undefined`.
- **Symbol**: Introducido en ECMAScript 6, representa un valor único e inmutable, utilizado principalmente como identificadores de propiedades de objetos.
- **BigInt**: Introducido en ECMAScript 2020, permite representar números enteros muy grandes que exceden el límite de los números de tipo `Number`.

ECMAScrip es un estandar para lenguajes de scripting siendo _JavaScript_ la implementación más conocida de este estándar. Más información puedes ver [MDN](https://developer.mozilla.org/es/docs/Glossary/ECMAScript).

## Tipos de datos no primitivos
Los tipos de datos no primitivos en JavaScript incluyen:
- **Object**: Es una colección de propiedades, donde cada propiedad es una asociación entre un nombre (clave) y un valor. Los objetos pueden contener otros objetos, funciones y tipos de datos primitivos. Ejemplo:
```javascript
let persona = {
    nombre: "Juan",
    edad: 30,
    esEstudiante: false
};
```
- **Array**: Es un tipo especial de objeto que representa una lista ordenada de valores. Los arrays pueden contener elementos de diferentes tipos de datos, incluidos otros arrays y objetos. Ejemplo:
```javascript
let numeros = [1, 2, 3, 4, 5];
let mezclado = [1, "dos", true, { clave: "valor" }, [6, 7, 8]];
```
- **Function**: En JavaScript, las funciones son también objetos y pueden ser tratadas como tales. Pueden ser asignadas a variables, pasadas como argumentos a otras funciones y retornadas desde funciones. Ejemplo:
```javascript
function saludar(nombre) {
    return "Hola, " + nombre + "!";
}
console.log(saludar("María"));
> "Hola, María!"
```
## Conversión de tipos
JavaScript realiza conversiones de tipos de datos de manera automática (coerción) en ciertas situaciones, como en operaciones aritméticas o comparaciones. También es posible realizar conversiones explícitas utilizando funciones como `String()`, `Number()`, `Boolean()`, entre otras. Por ejemplo:
```javascript
let numero = 42;
let texto = String(numero);         // Conversión explícita a String
> '42'
let booleano = Boolean(1);          // Conversión explícita a Boolean
> true
```
Entender los tipos de datos en JavaScript es fundamental para escribir código efectivo y evitar errores comunes relacionados con la manipulación de datos.
## Ejemplos prácticos
```javascript
// Ejemplo de tipos de datos primitivos
let numero = 100;                       // Number
let texto = "Hola, Mundo!";             // String
let esVerdadero = true;                 // Boolean
let sinValor;                           // Undefined
let valorNulo = null;                   // Null
let simbolo = Symbol("id");             // Symbol
let numeroGrande = 9007199254740991n;   // BigInt
// Ejemplo de tipos de datos no primitivos
let persona = {
    nombre: "Ana",
    edad: 25
};                                      // Object    
let frutas = ["Manzana", "Banana", "Cereza"]; // Array
```

