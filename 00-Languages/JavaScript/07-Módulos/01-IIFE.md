# IIFE's

Funciones Inmediatamente Invocadas de JavaScript.

```js
const weekDay = (function () {
  const names = [
    "Domingo",
    "Lunes",
    "Martes",
    "Miercoles",
    "Jueves",
    "Viernes",
    "Sabado",
  ];
  return {
    name: function name(number) {
      return names[number];
    },
    number: function number(name) {
      return names.indexOf(name);
    },
  };
})();

console.log(weekDay.name(5)); // Viernes
console.log(weekDay.number("Domingo")); // 1
```

Aquí podemos ver que dentro de la constante `weekDay` hemos guardado una function que contiene un arreglo y dos funciones con [closure](../04-FOUNDATIONS//01-JS_Avanzado/04-Closures.md).
