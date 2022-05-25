# Variables

Las **variables** se usan como recipientes, es la forma de almacenar algo para usar más tarde.

## Declarar Variables

Para declarar una variable se usa una **keyword**, seguida de un espacio, el **identificador** y le asignamos un valor con `=` .

- **Keywords:**
  Hay 3 keywords para declarar una variable:

  - `var:` Declara una variable con un alcance/_scope_ global, se le puede cambiar su valor.

  - `let:` Tiene un solo un alcance en el _bloque de código_ donde se ha declarado. Se le puede cambiar su valor luego.

  - `const:` Declara una variable en un bloque, no se puede cambiar el valor una vez declarada.

- **Identificadores:**
  Nombre de nuestro recipiente. Debe comenzar con:

  - Una letra (Aa - zZ)
  - Un signo de dólar `$`
  - Un guión bajo `_`
    > NUNCA con números o caracteres especiales.

```js
var a = 3;
a = 5;

let b = 2;
b = 10;

const name = "Alexis";
name = "Juan"; // la sintaxis dará 'error'
```

---

## Typeof

El operador es utilizada para obtener el tipo de dato que tiene una variable. Ejemplo:

```js
var saludo = "Hola";
let edad = 20;
var objeto = {};
let menorDeEdad = false;

typeof saludo; // string
typeof edad; // number
typeof objeto; // object
typeof menorDeEdad; // boolean
typeof mascota; // undefined, porque no fue creado
```
