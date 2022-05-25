## Expresiones vs Statements

Podemos decir que todo el código que escribimos en JS "hace algo" o "retorna algo" (o una combinación de los dos). En la terminología de lenguajes de programación esta diferencia está clasificada en la definición de **expressions** (expresiones) y **statements** (sentencias).

Podriamos definir conceptualmente a ambas como:

- Una **expression** siempre se convierte (retorna) un valor.

```js
// retorna algo
1 + 1;
Math.pow(2, 3) + 4;
"hola" + " soy una expression";
```

- Un **statement** realiza una acción.

```js
// hace algo
if (condicion) {
  // código ejecutado si es true
} else {
  // código ejecutado si es false
}
```

> Nos podemos dar cuenta que algo es un statement, porque si lo _pegamos_ en la _consola_ del intérprete -por ejemplo, en la consola del Firefox o Chrome- vamos a ver que no produce ningún resultado:

```js
    // expresiones!
    console.log(1 + 1);
    console.log(Math.pow(2,3) + 22);

    // statements!
    console.log(if( true) {
      // código
    });
    // jamás haríamos esto de arriba, no?
```
