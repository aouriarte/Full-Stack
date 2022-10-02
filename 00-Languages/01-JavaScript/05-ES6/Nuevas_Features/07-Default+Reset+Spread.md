# Default + Reset + Spread

```js
// Default
function suma(x, y = 12) { 
  return x + y;
};

suma(3);
// 15
```

Cuando hacemos funciones podemos pasar valores en el parámetro que estén por defecto. Este parámetro no se podrá cambiar.

```js
// Default + Destructuring
var [a, b, c] = [1, 2];
// En este caso, "c", tiene como valor undefined.

var [a, b, c = 3] = [1, 2];
// Aquí también podemos establecer un valor predefinido.

var [a, b, c = a + b] = [1, 2];
// a = 1
// b = 2
// c = 3
```

También podemos establecer valores predefinidos en la **_desestructuración_**.

```js
// Spread
function hola(x, ...y) {
  return x * y.length;
};

hola(3, "hello", true);
// 6
```

Cuando pasamos por parámetro la condición “. . . _y_”, lo que sucederá es que podremos pasar todos los parámetros que queramos. Estos argumentos se acumularán en un _array_.

```js
var arr = [1, 2, 3];

function f(x, y, z) {
  return x + y + z;
};

f(...arr);
// 6

f(arr);
// 1, 2, 3undefiendundefined

f(arr, arr, arr);
// 1, 2, 31, 2, 31, 2, 3
```
