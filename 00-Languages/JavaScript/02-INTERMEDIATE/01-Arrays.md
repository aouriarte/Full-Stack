# Arrays (matrices/ arreglos)

Es un _"objeto tipo lista"_. Al igual que una variable sirve de recipiente, pero los arreglos o _matrices_ pueden almacenar más elementos, como una lista.

## Crear un array

Para construir un arreglo, declaramos una variable y la establecemos en `[]` . Luego podemos agregar cualquier tipo de dato o elementos separados por comas dentro del contenedor.

```js
let frutas = ["Manzana", "Banana", "Pera"];

console.log(frutas.length); //3
```

> **.lenght:** Este método que también lo tiene el tipo de dato _String_, viene en los arreglos. La matriz `.length` devolverá el número de elementos de un _array_.

## Acceder a elementos de una matriz

Para acceder a un elemento de un arreglo solo necesitamos llamarlo por su posición (índice) dentro de ella:

> Las computadoras comienzan a contar desde 0, así que SIEMPRE el elemento principal comenzarán con ese índice.

```js
var lista = ["Alexis", 20, true];
                 0     1     2

// accedemos al primer elemento:
console.log(lista[0]);
// Alexis

// accedemos al último elemento:
console.log(lista[lista.length - 1]);
// true
```

## Asignar y Reasignar elementos

Podemos asignar y reasignar elementos con los `[]`, índice y un `=` .

```js
var lista = ["Alexis", 20, true];

lista[0] = "Orlando";

console.log(lista); // ['Orlando', 20, true]
```

## Añadir y Eliminar elementos

Más métodos de _array_:

### .push()

AÑADE un elemento al FINAL de la matriz:

```js
var frutas = ["Manzana", "Banana", "Naranja", "Pera"];

frutas.push("Uva"); // puedes agregar más

console.log(frutas); // ['Manzana', 'Banana', 'Naranja', 'Pera', 'Uva'];
```

### .pop()

ELIMINA el ÚLTIMO elemento de la matriz:

```js
var frutas = ["Manzana", "Banana", "Naranja", "Pera", "Uva"];

frutas.pop();

console.log(frutas); // ['Manzana', 'Banana', 'Naranja', 'Pera'];
```

### .unshift()

AÑADE un elemento al INICIO de la matriz:

```js
var frutas = ["Manzana", "Banana", "Naranja", "Pera"];

frutas.unshift("Fresa");

console.log(frutas); // ['Fresa', 'Manzana', 'Banana', 'Naranja', 'Pera'];
```

### .shift()

ELIMINA el elemento que está al INICIO de la matriz:

```js
var frutas = ["Fresa", "Manzana", "Banana", "Naranja", "Pera"];

frutas.shift("Fresa");

console.log(frutas); // ['Manzana', 'Banana', 'Naranja', 'Pera'];
```

## Recorrer un array

La mayoría de las veces los bucles **for** se usan para iterar (recorrer) sobre todos los elementos de un arreglo:

```js
let frutas = ["Manzana", "Banana", "Pera"];

for (let i = 0; i < frutas.length; i++) {
  console.log(frutas[i]);
}

// "Manzana"
// "Banana"
// "Pera"
```

---

## Métodos del Array

### .forEach()

Este método sirve como iterador para ejecutar una función una vez por cada _elemento_ del arreglo.

**Sintaxis:**

    array.forEach(function callback(element, index, array){
    // tu iterador o instrucción
    });

- **function:** Función que se llama (callback). Recibe 3 argumentos:
  - **element:** Elemento del arreglo.
  - **index:** Posición del elemento (opcional).
  - **array:** El arreglo donde se llamó el método (opcional).

```js
var tablaDeDos = [1, 2, 3, 4];

// podemos escribir el 'callback como una función anónima
tablaDeDos.forEach(function (element) {
  console.log(element * 2); //2, 4, 6, 8
});

// o podemos crear una nueva función para usarla como 'cb'.
// y ya no necesitaríamos usar el argumento de 'element'.
function multiplicar(element) {
  console.log(element * 2);
}

// y llamas esa función
tablaDeDos.forEach(multiplicar);
```

### .reduce()

Este método recorre todos los elementos del arreglo (de izq. a der.). Aplica una función _reductora_ a cada uno de los valores del arreglo (los _acumula_), y devuelve como resultado _un solo valor_.

**Sintaxis:**

    array.reduce(function callback(acc, element, index, array){
        //instrucción
    },valorInicial);

- **function:** Nuevamente un callback, que siempre debe contar con un return.
  Recibe los parámetros: 
  + **acc:** Acumulador. Sería el resultado de la _reducción_. 
  + **element:** Elemento del arreglo. 
  + **index:** Posición del elemento. (opcional) 
  + **array:** El arreglo donde se llamó el método. (opcional) 
  + **valorInicial:** Si está presente se toma como primer argumento en la función, como primer elemento. (opcional)

```js
var numeros = [1, 2, 3, 4];

//1.podemos hacer una función anónima
//si omitimos el valorinicial, siempre comenzará en el primer elemento del arreglo
var suma = numeros.reduce(function (acc, element) {
  return acc + element;
});

// o podemos crear una función para usarla como 'cb'
function multiplicar(a, b) {
  return a * b;
}

var total = numeros.reduce(multiplicar);

//2.este método funciona con cualquier tipo de dato
// ejemplo poniendo 'valorInicial':
var verso = ["tu", "sonrisa", "era", "mi", "poema", "favorito."];

var frase = verso.reduce(function (acc, element) {
  return acc + " " + element;
}, "Te lo digo:");

console.log(suma); // 10
console.log(total); // 24
console.log(frase); // 'Te lo digo: tu sonrisa era mi poema favorito.'
```

### .map()

Crea un nuevo arreglo con los resultados de la llamada a la función indicada aplicados a cada uno de sus elementos. Al igual que los métodos anteriores tiene `index` y `array` como opcionales.

```js
var numeros = [1, 2, 3, 4, 5];

// podemos crear un function anónima o crearla aparte para llamarla luego
var tablaDelDiez = numeros.map(function (element) {
  return element * 10;
});

console.log(tablaDelDiez); // [10, 20, 30, 40, 50]
```
