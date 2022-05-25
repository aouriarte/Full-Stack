## Statements (sentencias)

Los **Statements** son instrucciones que le damos al intérprete de JS para que _haga algo_, ese algo puede ser: crear una variable, ejecutar un bloque de código N veces, ejecutar un bloque de código o no según una condición de verdad, declarar una función, etc.

Podemos clasificar a los Statements en las siguientes categorías:

### **Declaration Statements**

Este tipo de statements indican al intérprete que declare variables o funciones, se utiliza el keyword `function` y `var` :

```js
var prueba; // declaro la variable prueba
var toni; // declaro la variable toni

function suma(a, b) {
  // declaro la función suma;
  // bloque de código
}
```

> Habiamos dicho que por regla general lo que podamos pasarle a una función (por ejemplo, `console.log`) por argumento era una expresión... y muchas veces pasamos una declaración de una función por argumento. Esto sucede porque en JS existen tambien las **function expressions**.

### **Function Expressions vs Function Declarations:**

Cuando declaramos una función el intérprete puede _interpretarla_ como un statement o cómo una expresión, dependiendo del contexto. Por ejemplo:

```js
// function declaration:
function resta(a, b) {
  // bloque de código
}

// function expression:
var resta = function (a, b) {
  // bloque de código
};

array.map(function () {
  // código;
});
// el argumento de la función espera una expression

// immediately Invoked Function Expression
(function () {
  console.log("IIFE");
})();
```

Cómo vemos en el ejemplo de arriba, el intérprete _hace algo_: declara la función. Por lo tanto es un statement. En cambio, en el segundo ejemplo, estamos haciendo una asignación, y la asignación espera una **expresión** en la parte de la derecha, asi que le estamos pasando un function expression.

> Nótese que un function expression puede no tener nombre. Estas son las llamadas **funciones anónimas**.

### **Conditional Statements**

Estos statements sirven para controlar el flujo de ejecución de código según si se cumple o no una condición. Por ejemplo:

```js
if (condicion) {
  // condicion puede ser cualquier expression!!
  // ejecuta este bloque si condicion es true
} else if (condicion2) {
  // ejecuta este bloque de código si condicion no es true y condicion2 es true
} else {
  // ejecuta este bloque de código si condicion y condicion2 no son true.
}
```

### **Loops (bucles) y Jumps (saltos)**

Estos statements también controlan el flujo de ejecución del código, pero hacen que un bloque se ejecute N veces (ej: `for`), o que la ejecución salte a otro contexto (ej: `return`). Por ejemplo:

```js
// loops
while(condicion){ // condicion es una expresión!!
  // ejecuta este código mientras condicion sea true;
}

for(var i = 1; i < 10; i++){
  // ejecuta este bloque de código 9 veces;
}

// jumps
function(){
  // bloque de código
  return;  // cuando llegue acá, sale de la ejecución de la función y retorna un valor;
  // bloque de código
}

for(var i = 1; i < 10; i++){
  // ejecuta este bloque de código N veces;
  continue; // salta a la siguiente iteración del bucle;
  // desde acá no se ejecuta;
}

throw new Error('hubo un error, se termina la ejecución');
```

### **Expression Statements**

JS tiene la particularidad qué en donde sea que el intérprete espera un _statement_, nosotros podemos pasarle una _expresión_. Esto da lugar a los llamados _expression statements_.

> **Esto no funciona en sentido inverso, donde se espera una expresión _NO_ podemos pasar una statement**.
