# Operadores

En javascript vamos a poder realizar operaciones a través de los _operadores_.

## Operadores Aritméticos

Los operadores estándar son tal cual los que funcionan en una calculadora: (`+`, `-`, `/`, `*`)

```js
var suma = 1 + 1; // 2
var resta = 5 - 2; // 3
var división = 9 / 3; // 3
var multiplicación = 4 * 6; // 24
```

Además de los estándar, tenemos los siguientes:

### **Residuo**

Corresponde al _módulo_ de una operación, quiere decir que nos devulver el resto de una división.

```js
var a = 12 % 5; // 2
```

### **Incremento**

Incrementa en una unidad al operando. Si es usado `++x` devuelve el valor _después_ de añadirle 1. Si se usa `x++` devulve el valor _antes_ de añardirle 1.

```js
var x = 3;
var b = ++x; // 4

var y = 3;
var c = y++; // 3
```

### **Decremento**

Tiene el mismo comportamiento que el incremento, solo que esta vez se le resta.

```js
var x = 3;
var b = --x; // 2

var y = 3;
var c = y--; // 3
```

## Operadores de Asignación

Continuando con los operaciones de aritmética, podemos usar esos operadores al asignar nuevamente un valor con `=`:

```js
var a = a + 1; // abreviado a += 1
var b = b - 2; // b -= 2
var c = c / 3; // c /= 3
var d = d * 4; // d *= 4
var e = e % 5; // e %= 5
```

## Operadores de Comparación

### **Igualdad:**

Devuelve `true` si ambos operandos (datos) son iguales (`==`).

```js
1 == "1"; // true
```

### **Desigualdad:**

Devuelve `true` si los operandos no son iguales (`!=`).

```js
7 != 5; // true
8 != "8"; // false
```

### **Estrictamente Igual:**

Devuelve `true` si los operandos son iguales y del mismo tipo (`===`).

```js
1 === "1"; // false
```

### **Estrictamente Desigual:**

Devuelve `true` son del mismo tipo pero no iguales, o son de difente tipo(`!==`).

```js
5 !== 5; //false
6 !== "6"; //true
```

#### **Mayor que:**

Devuelve `true` si el operando izquierdo es _mayor_ que el derecho. (`>`).

```js
3 > 4; //false
```

#### **Mayor o Igual que:**

Devuelve `true` si el operando izquierdo es _mayor_ o _igual_ que el derecho. (`>=`).

```js
100 >= 100; //true
```

#### **Menor que:**

Devuelve `true` si el operando izquierdo es _menor_ que el derecho. (`<`).

```js
2 < 3; //true
```

#### **Menor o Igual que:**

Devuelve `true` si el operando izquierdo es _menor_ o _igual_ que el derecho. (`<=`).

```js
10 <= 1; //false
```

## Operador Ternario

Se usa con frecuencia como atajo de la instrucción `if` . Necesita 3 operando:

### Sintaxis:

    condición ? valor1 : valor2

Si la condición es `true` tomará el valor 1, sino el valor 2.
También se puede poner código adentro, al igual que `if` .

```js
var stop = false,
  edad = 23;

edad > 18
  ? (alert("OK, puedes continuar."), location.assign("continue.html"))
  : ((stop = true), alert("Disculpa, eres menor de edad!"));
```

## Operadores Lógicos

También podemos combinar dos expresiones de igualdad y preguntar si alguna de las dos es verdadera, si ambas son verdaderas o sin ninguna lo es.

### **Y (AND)**

Devolverá `true` si AMBAS son verdaderas, de lo contraria si alguna o ambas son falsas dará `false` . Se escribe `&&` .

```js
if (100 > 10 && 10 === 10) {
  console.log("AMBAS declaraciones son ciertas, este código se ejecutará");
}

if (10 === 9 && 10 > 9) {
  console.log(
    "UNA de las declaraciones es false, por lo que && devolverá false, y este código no se ejecutará"
  );
}
```

### **O (OR)**

Devolverá `true` si AMBAS o UNA de las expresiones es verdadera. Dará `false` si ambas son falsas. Se escribe `||` .

```js
if (100 > 10 || 10 === 10) {
  console.log("AMBAS declaraciones son ciertas, este código se ejecutará");
}

if (10 === 9 || 10 > 9) {
  console.log(
    "UNA de las declaraciones es true, por lo que || devolverá true y este código se ejecutará"
  );
}

if (10 === 9 || 1 > 9) {
  console.log(
    "AMBAS declaraciones son FALSAS, por lo que || devolverá false y este código no se ejecutará"
  );
}
```

### **NOT**

Devolverá el valor booleano del que se le pasa. Se escribe `!` .

```js
if (!false) {
  console.log(
    "El ! devolverá true, porque es lo contrario de false, así que este código se ejecutará"
  );
}

if (!(1 === 1)) {
  console.log(
    "1 es igual a 1, de modo que la expresión devuelve true. El operador ! devolverá lo contrario de eso, por lo que este código NO se ejecutará"
  );
}
```

---

## Precedencia y Asociatividad de Operadores

- **Precedencia:**

La precedencia determina el _orden en el cual se realiza una operación_, el operador de mayor precedencia se ejecuta primero. Algo parecido a las matemáticas.

```js
3 + 4 * 5; //retorna 23
```

- **Asociatividad:**

Cuando los operadores son de igual precedencia se desarrolla de _derecha a izquierda o viceversa_. Podemos ver la documentación completa o la tabla de asociatividad [Aquí](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Operators/Operator_Precedence).
