## Closures

Las Clausuras se conocen como funciones _anidadas_ (es una función que retorna otra función). Nos guarda información en la memoria para usarla luego, información asociada.

```js
function producto(a) {
  return function (b) {
    return a * b;
  };
}
```

Ejemplo1:

```js
// tabla del 2
var producto2 = producto(2); // se lleva a la función 'b'
      // function(b) {
      //  return a * b;
      // }
for(let i = 0, i < 11; i++) {
  console.log(producto2(i));
}

var producto3 = producto(3); // se cambia el parámetro 'a' por 3
```

Ejemplo2:

```js
var crearFuncion = function () {
  var arreglo = [];

  for (var i = 0; i < 3; i++) {
    arreglo.push(function () {
      console.log(i);
    });
  }
  return arreglo;
};

var arr = crearFuncion();

arr[0](); // 3, nos da 3 porque en memoria quedo ese único valor al llamar 'crearFuncion'
arr[1](); // 3, ya no puede llamarlo en cada paso
arr[2](); // 3, porque ya se destruyo el contexto de ejecución de esa función.

/* memory:
arreglo: [function(){console.log(i)} 'aca sería 1' , function(){console.log(i)} 'sería 2', function(){console.log(i)} 'sería 3' y se corto el 'for'] --> una vez esto se destruye este contexto.

i: 3, la información que se guardó.
*/

// pero si queremos que nos imprima cada paso, podemos hacer esto:
var creaFuncion = function () {
  var array = [];

  for (var i = 0; i < 3; i++) {
    array.push(
      (function (j) {
        // copia el valor de 'i'
        return function () {
          console.log(j);
        }; // lo imprime
      })(i)
    ); // 'i' parámetro que se la pasa a la función. i = f
  }
  return array;
};

var arr = creaFuncion();

arr[0](); // 0
arr[1](); // 1
arr[2](); // 2
// i = 3;
```
