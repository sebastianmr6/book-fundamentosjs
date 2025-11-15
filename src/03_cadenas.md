# Manipulación de cadenas

Las cadenas de texto, o _strings_, son una secuencia de caracteres utilizados para representar texto en JavaScript. Las cadenas pueden ser definidas utilizando comillas simples (`'...'`), comillas dobles (`"..."`) o backticks (`` `...` ``) para plantillas literales.

## Creación de cadenas

```javascript
let cadena1 = 'Hola, Mundo!';               // Comillas simples
let cadena2 = "Hola, Mundo!";               // Comillas dobles
let cadena3 = `Hola, Mundo!`;               // Backticks (plantillas literales)
```
## Operaciones comunes con cadenas
### Concatenación
La concatenación de cadenas se puede realizar utilizando el operador `+`, interpolación de cadenas (template literals) o el método `concat()`.
```javascript
let saludo = 'Hola, ' + 'Mundo!';           // Usando +
console.log(saludo);
> "Hola, Mundo!"

let nombre = 'Juan';
let saludo2 = `Hola, ${nombre}!`;            // Usando template literals
console.log(saludo2);
> "Hola, Juan!"

let saludo3 = 'Hola, '.concat('Mundo!');    // Usando concat()
console.log(saludo3);
> "Hola, Mundo!"
```
### Longitud de una cadena
Puedes obtener la longitud de una cadena utilizando la propiedad `length`.
```javascript
let texto = 'Hola';
console.log(texto.length);
> 4
```
### Acceso a caracteres
Puedes acceder a caracteres individuales de una cadena utilizando la notación de corchetes o el método `charAt()`.
```javascript
let texto = 'Hola';
console.log(texto[0]);
> "H"
console.log(texto.charAt(1));
> "o"
```
### Métodos comunes de cadenas
- `toUpperCase()`: Convierte la cadena a mayúsculas.
- `toLowerCase()`: Convierte la cadena a minúsculas.
- `concat()`: Une dos o más cadenas.
- `trim()`: Elimina los espacios en blanco al inicio y al final de la cadena.
- `slice()`: Extrae una sección de la cadena y devuelve una nueva cadena.
- `replace()`: Reemplaza una parte de la cadena por otra.
- `split()`: Divide la cadena en un array de subcadenas basándose en un separador.
```javascript
let texto = '  El análiis espacial es genial, ¡usar los Sensors Remotos es increíble!  ';
console.log(texto.toUpperCase());
> "  EL ANÁLIIS ESPACIAL ES GENIAL, ¡USAR LOS SENSORS REMOTOS ES INCREÍBLE!  "
console.log(texto.toLowerCase());
> "  el análiis espacial es genial, ¡usar los sensors remotos es increíble!  "
console.log(texto.concat(' ¿Cómo estás?'));
> "  El análiis espacial es genial, ¡usar los Sensors Remotos es increíble!   ¿Cómo estás?"
console.log(texto.trim());
> 'El análiis espacial es genial, ¡usar los Sensors Remotos es increíble!'
console.log(texto.slice(2, 7));
> "El an"
console.log(texto.replace('Sensors Remotos', 'JavaScript'));
> "  El análiis espacial es genial, ¡usar los JavaScript es increíble!  "
console.log(texto.split(', '));
> ['  El análiis espacial es genial', '¡usar los Sensors Remotos es increíble!  ']
```
Entender cómo manipular cadenas es esencial para trabajar con texto en JavaScript, ya que muchas aplicaciones requieren procesamiento y manipulación de datos textuales.