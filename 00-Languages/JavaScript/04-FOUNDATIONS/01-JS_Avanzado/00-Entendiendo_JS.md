# Entendiendo JS

## SINGLE THREADED Y SINCRÓNICO

Un _thread_ (o hilo de ejecución) es la secuencia de instrucciones más pequeña que puede ser manejada por un planificador de recursos (se encarga de repartir el tiempo disponible de los recursos del sistema entre todos los procesos).

JavaScript es _Single Threaded y Sincrónico_, quiere decir que sólo puede hacer p ejecutart una sola instrucción (comando) a la vez y lo hace en orden. Se conoce como _execution stack_ (ejecución de pila).

## Lexical Enviroment

El _Entorno Léxico_ tiene que ver con dónde están declarados ciertos **statements o expresiones** en tu código. No será lo mismo hacerlo en un lugar que en otro. Lugar en donde se van almacenar las variables y parámetros de una función

Por ejemplo, para el intérprete las dos declaraciones de variable del arriba tendrán signicados muy distintos, ya que al estar en lugares distintos (una dentro de una función y la otra no) el intérprete las parseará (las leerá) de forma distinta:

```js
function hola() {
  var foo = "Hola!";
}
var bar = "chao!";
```

> **Global Enviroment:** es la ventana “padre” del código. El la parte más externa, la que envuelve a todo el código. Dentro de este contexto podremos encontrar otros contextos.

---

## Execution Context

El _contexto de ejecución_ contiene información sobre **QUÉ** código se está ejecutando en cada momento. Esto se da en las `functions` . Trabaja como pila, primero se hace algo luego otro, como las muñecas _Matrioshka_.

```js
// global context
var diceHola = "Hola";

// Cada vez que se crea una nueva 'function' se crea un nuevo contexto de ejecución.
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
