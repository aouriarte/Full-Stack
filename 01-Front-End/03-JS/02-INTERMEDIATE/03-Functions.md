# Funciones

Son un tipo de **objetos** particulares llamados _callable objects_ u obsjetos incovables. Se componen por un conjunto o secuencia de declaraciones (variables).

## Contruir una Función

Hay 3 formas de hacerlo:

```js
function primera() {}
var segunda = function () {};
var tercera = () => {};
```

### Sintaxis

Se usa la palabra clave `function` , después viene el nombre de la función que indica lo que hace. Luego vienen los `()` donde van los _argumentos_ y vienen las llaves donde se declaran las variables o instrucciones:

- **argumentos**

Son parámetros de nuestra función que se pasan por _valores_. Pueden haber muchos argumentos.

```js
function sumarNumeros(a /* arg1 */, b /* arg2 */) {
  var suma = a + b; // instrucciones
  return suma; // retorna ese valor
}

sumarNumeros(10 + 5); // 15
console.log(suma); // undefined
```

- **return**

Para devolver un valor específico nuestra función debe tener una _sentencia_ `return` .
Es como lo único que escapa. Lo único a lo que se accede cuando llamamos a la función. Si intentamos llamar a algo que está dentro de la función con `console.log` nos dará `undefined`. Esto por el _scope_.

También podemos crear variables para igualar a lo que devuelve la función.

```js
function restarNumeros(a, b) {
  var resta = a - b;
  return resta;
}

var diferencia = restarNumeros(10 - 5);
console.log(diferencia); // 5
console.log(resta); // undefined
```
