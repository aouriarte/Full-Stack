# Estructura de Datos

Manera de organizar los datos en la programación.

## Lineales

Están los 'Queues'(Colas), 'Stacks'(Pilas)

### Stacks

Las pilas PUSH (agrega un valor al último) - POP (elimina el último valor y lo devuelve).
Se manejan en LIFO (Last In, First Out). Lo último en llegar lo primero en salir.

```js
var stack = [];
stack.push(1); // [1]
stack.push(2); // [1,2]
stack.push(5); // [1,2,5]

let i = stack.pop(); // [1,2] i = 5
console.log(i);
let j = stack.pop(); // [1] j = 2
console.log(j);
```

---

### Queues

Las colas. Se manejan con FIFO (First In, Firt Out). El primero en llegar el primero en irse.

```js
var queue = [];
queue.push(1); // [1]
queue.push(2); // [1,2]
queue.push(5); // [1,2,5]

let i = queue.shift(); // [2,5] i = 1
console.log(i);
let j = queue.shift(); // [5] j = 2
console.log(j);
```

---

## No Lineales

Están los 'trees'(árboles),
