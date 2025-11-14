## Variables en JavaScript

Una variable es un contenedor para almacenar datos, que puede cambiar durante la ejecución del programa. Se debe declarar antes de usarla y puede contener diferentes tipos de datos como números, cadenas de texto, objetos, etc.

La declaración se realiza a través de las palabras reservadas `var`, `let` o `const`, seguidas del nombre de la variable y, opcionalmente, un valor inicial.

```javascript
var nombreVar = "Juan";
let nombreLet = "Ana";
const nombreConst = "Luis";
```

El uso de `var` es más antiguo y tiene un alcance de función, mientras que `let` y `const` tienen un alcance de bloque, siendo `const` para valores que no deben ni pueden cambiar.

Se desaconseja el uso de `var` en favor de `let` y `const` debido a problemas de alcance y hoisting.

Nota: Durante este tutorial verás que se usa `console.log()` para mostrar información en la consola del navegador o del entorno de ejecución, esto lo que hace es que imprimirá en la consola el valor de la variable o el resultado de alguna expresión, también verás el símbolo `>` que indica la salida o resultado de una operación en la consola.

**¿Qué es el alcance de una variable?:** El alcance determina la visibilidad de una variable en diferentes partes del código. 

- Alcance de `var`: es a nivel de función y no a nivel de bloque. presenta prblemas pues permite acceder a la variable fuera del bloque donde fue declarada y puede causar confusión, también puede ser redeclarada dentro del mismo ámbito.

```javascript
// Problema: Redeclaración permitida
var nombre = "LANDSAT";
var nombre = "Sentinel";            // No genera error
console.log(nombre);                
> "Sentinel"
```

- Alcance de `let` y `const`: tienen alcance de bloque, lo que significa que solo son accesibles dentro del bloque donde fueron declaradas (entre llaves `{}`). Esto evita confusiones y errores comunes.

```javascript
// Ejemplo: Alcance de bloque con let
if (true) {
    let edad = 30;
    console.log(edad);              // 30
}
console.log(edad);                  // Error: edad no está definida

// Ejemplo: Alcance de bloque con const
if (true) {
    const PI = 3.14;
    console.log(PI);                // 3.14
}
console.log(PI);                    // Error: PI no está definida 
```


- Una función es un bloque de código diseñado para realizar una tarea específica. Se define utilizando la palabra clave `function`, seguida del nombre de la función, paréntesis y llaves que contienen el código a ejecutar. Esto lo veremos en el capítulo de funciones pero puedes tomar en cuenta el siguiente ejemplo de los problemas de var al usar funciones:

El uso de `var` dentro de una función permite acceder a la variable fuera del bloque donde fue declarada, lo que puede causar confusión.
```javascript
function ejemploVar() {
    if (true) {
        var mensaje = "Hola desde var";
    }
    console.log(mensaje);              // "Hola desde var" (acceso permitido)
}
ejemploVar();
```

Caso contrario con `let` y `const` pues esto no es posible:
```javascript
function ejemploLetConst() {
    if (true) {
        let mensajeLet = "Hola desde let";
        const mensajeConst = "Hola desde const";
    }
    console.log(mensajeLet);           // Error: mensajeLet no está definida
    console.log(mensajeConst);         // Error: mensajeConst no está definida
}
ejemploLetConst();
```

- El hoisting es un comportamiento en JavaScript donde las declaraciones de variables y funciones son movidas a la parte superior de su ámbito antes de la ejecución del código. Esto puede llevar a resultados inesperados, especialmente con `var`.
En el siguiente ejemplo, la variable `miVariable` es accesible antes de su declaración debido al hoisting, pero su valor es `undefined` hasta que se asigna un valor.

```javascript
// Problema: Hoisting confuso
console.log(miVariable); // undefined (no error)
var miVariable = "Hola mundo";
```

Si se usa `let` o `const`, acceder a la variable antes de su declaración genera un error, lo que ayuda a evitar confusiones.

```javascript
// Ejemplo: Hoisting con let/const
console.log(miVariableLet); // Error: miVariableLet no está definida
let miVariableLet = "Hola mundo";
```

En algunas partes las variables son escritas en inglés para mantener consistencia con la mayoría de la documentación técnica, pero es recomendable usar el idioma que mejor se adapte al equipo de desarrollo. Las variables deben ser descriptivas y seguir una convención de nomenclatura consistente. 

### Tipo de formas comunes para nombrar variables:
1. **camelCase**: La primera palabra en minúscula y las siguientes con la primera letra en mayúscula.
    ```javascript
    let nombreDeLaMision = "Landsat";
    ```
2. **snake_case**: Todas las palabras en minúscula separadas por guiones bajos.
    ```javascript
    let nombre_de_la_mision = "Sentinel - 2";
    ```
3. **PascalCase**: Todas las palabras con la primera letra en mayúscula.
    ```javascript
    let MejorCursoDeLaCarrera = "Sistemas de Información Geográfica";
    ```

### Buenas prácticas para nombrar variables:

1. **Usar nombres descriptivos**
    ```javascript
    let edadUsuario = 25;
    ```

2. **Usar camelCase para múltiples palabras**
    ```javascript
    let numeroDeEstudiantes = 30;
    ```

3. **Evitar usar palabras reservadas del lenguaje**
    ```javascript
    let for = 10; // Incorrecto
    ```

4. **No comenzar con números**
    ```javascript
    let 1nombre = "Pedro"; // Incorrecto
    ```

5. **Usar minúsculas para la primera letra (camelCase)**
    ```javascript
    let ciudadNacimiento = "Madrid";
    ```

