# Entendiendo JS

El proceso de ejecución en Javascript es _sincrónico_, quiere decir que se ejecuta un código a la vez. Se conoce como _execution stack_ (ejecución de pila).

## Lexical Enviroment

El Entorno Léxico tiene que ver con los contextos de ejecución (scope). Lugar en donde se van almacenar las variables y parámetros de una función.

## Execution Context

Contiene información sobre que código se está ejecutando en cada momento. Además de mantener el código que tiene que tiene que ejecutar, también mantiene más información sobre donde se invocó ese código, en qué _lexical enviroment_ está.
_Trabaja como pila_, primero se hace algo luego otro, como las muñecas _Matrioshka_.

```js
// global context
var diceHola = "Hola";

function person() {
  // execution context (llaves amarillas)
  var first = "David";
  last = "Pérez";

  function firstName() {
    // execution context (rosado)
    return first;
  }

  function lastName() {
    // execution context (rosado)
    return last;
  }

  console.log(diceHola + firstName() + " " + lastName());
}
```

> Tiene que ver con el **scope**.
