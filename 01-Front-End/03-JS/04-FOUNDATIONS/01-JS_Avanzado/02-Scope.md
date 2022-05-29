# Scope

Es el alcance que tiene una variable y desde donde se le puede llamar. Donde va a vivir.

## Tipos de Scope

- **Scope Global:** Las variables que creamos fuera de una función o bloque de código tienen un _alcance global_. Podemos acceder a ellas desde cualquier lugar de nuestro programa. Sin importar si las declaramos con `var` , `let` o `const` .

- **Scope Local:** Las variables locales sólo se pueden acceder desde una parte de nuetro programa. Tienen su alcance dentro de ese bloque de código.

> Cada variable es independiente si está dentro o no de un bloque de código, por eso podemos usar los mismos nombres de variables dentro de funciones o fuera de estas.

```js
var fruta = "manzana";

function comer() {
  // execution context
  var otraFruta = "banana";

  function lavar() {
    // execution context
    console.log("Lavando " + otraFruta); // aquí busca la variable en su contexto de execution 'lavar', no la encuentra, entonces busca en el otro contexto que la encierra 'comer' y ahi esta: "banana", si no la encontraba ahí, seguiría buscando hasta el contexto global.
  }

  lavar(); // 'Lavando banana'
  console.log("Comiendo " + otraFruta);
}

comer(); // antes de comer se lava la fruta
```

> Además en el caso tengamos las variables con el mismo nombre en ambos contextos de ejecución, este busca en su primer contexto y obvia el que está fuera en _outer context_. A esto se le llama _variable shadowing_.
