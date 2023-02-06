# Bucles e Iteracción

Los bucles ofrecen una forma rápida y sencilla de hacer algo repetidamente.

## For

Un bucle `for` se repite hasta que la condición especificada sea `false` .

```js
for (let i = 0; i < 10; i++) {
  // |Expresión Inicial   |Expresión Condicional  |Expresión De Actualización|
  // Sentencia o instrucción
  console.log(i);
}
```

- **Expresión Inicial:** Se ejecuta si existe. Inicia uno o más contadores de bucle.También puede declarar variables.
- **Expresión Condicional:** Se seguirá ejecutando hasta que el valor sea `false` y el bucle finaliza.
- **ExpresiónDeActuaización:** Actualizaremos nuestra variable. y se vuelve a evaluar la condición.
- **Sentencia o Instrucción:** Si el valor de la condición descrita es `true` se ejecuta la sentencia.

---

## While

Ejecuta sus setencias mientras la condición sea verdadera.

```js
let i = 0;
let x = 0;

while (i < 3 /* condición */) {
  i++; // expresión
  x = x + i; // x += i;
}
```

Con cada iteración, el bucle incrementa `i` y agrega ese valor a `x` . Por lo tanto, `x` e `i` toman los siguientes valores:

- Después de la primera iteración: `i` = 1 y `x` = 1
- Después de la segunda iteración: `i` = 2 y `x` = 3
- Después de la tercera iteración: `i` = 3 y `x` = 6

Después de completar la tercera iteración, la condición `i < 3` ya no es `true` , por lo que el bucle termina.

---

## Do...While

Esta instrucción se repite hasta que una condición específicada se evalúe como falsa.

```js
do {
  i = i + 1; // expresión, se itera al menos una vez
  console.log(i);
} while (i < 5); // condición, la expresión se vuelve a ejecutar hasta que `i` sea > 5
```

_Expresion_ se ejecuta una vez antes que se evalúe la condición. Si condición es `true` , la declaración se ejecuta de nuevo. Al final de cada ejecución, se comprueba la condición. Cuando la condición es `false` , la ejecución se detiene y el control pasa a la declaración que sigue a `do...while` .

---

## Bucles Infinitos

> Evita los bucles _infinitos_. Asegurate que la condición en un bucle llegue finalmente a ser `false`, o sino el bucel nunca terminará:

```js
for (let i = 0; i >= 0; i++) {
  // La condición nunca terminará, porque la variable ya esta declarada igual que 0 y además la expresión de actualización es de incremento, así nunca terminará
  console.log(i);
}
```

---

## For...in

Bucle para iterar sobre cada par _clave-valor_, itera una variable especificada sobre todas las propiedades enumerables de un objeto.

SINTAXIS:

    for (variable in objeto) {
    instrucción
    }

```js
const user = {
  username: 'alexisuriarte',
  password: 'contraseña',
  edad: 20,
};

for(let clave in user){
  console.log(clave); // imprimirá solo la 'clave'
  console.log(user[clave]); // imprimirá las claves y sus valores
}

// username
// 'alexisuriarte'
//  password
// 'contraseña'
//  edad
// 20
```
