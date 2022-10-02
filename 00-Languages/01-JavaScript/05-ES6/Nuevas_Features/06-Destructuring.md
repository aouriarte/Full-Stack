# Destructuring

```js
var [a, b, c] = [1, 2, 3];
// a = 1
// b = 2
// c = 3

var [d, , f] = [4, 5, 6, 7, 8];
// d = 4
// f = 6
```

Esta declaración permite otorgarle un valor a cada variable de forma ordenada entre corchetes.

Para saltearnos algunos valores debemos pasar **_espacios vacíos_**.

```js
var obj = {
  name: "Alexis",
  lastname: "Uriarte",
  job: {
    daytime: "alumno",
    nighttime: "batman",
  },
};

var {
  name,
  job: { daytime },
} = obj;
// Alexis, alumno
```

Con la estructura `var {} = ObjectName` , podemos desestructurar un objeto para obtener el valor de ciertas propiedades.

```js
function bar({ name }) {
  console.log(name);
};

bar(obj);
// Alexis
```

Cuando en el argumento de una función pasamos entre **llaves** la propiedad de un objeto, y cuando ejecutamos la función pasamos por parámetro el nombre del objeto, podremos utilizar el valor de esa propiedad en la estructura de la función.
