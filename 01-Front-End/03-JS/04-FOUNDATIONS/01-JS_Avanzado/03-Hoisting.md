# Hoisting

En Javascript permite llamar a una función o declaración sin haberla definido o declarado antes. Las variables y declaraciones son _elevadas_.

```js
bar(); // 'Soy una función'
console.log(foo); // undefined

var foo = "Hola, me declaro";
function bar() {
  console.log("Soy una función");
}
```

Las variables y las funciones declaradas como variables no están definidas por el _hoisting_ .Solo las funciones declaradas como statement serán reconocidas como una función completa (su instrucción se ejecuta).
