## Hoisting

En Javascript permite llamar a una función o declaración sin haberla definido o declarado antes. Las variables y declaraciones son _elevadas_.

```js
bar(); // 'Soy una función'
console.log(foo); // undefined

var foo = "Hola, me declaro";
function bar() {
  console.log("Soy una función");
}
```

> En el caso de la función, si declara su instrucción, pero el de la variable solo guarda en memoria un espacio para esa variable, más no su valor.
