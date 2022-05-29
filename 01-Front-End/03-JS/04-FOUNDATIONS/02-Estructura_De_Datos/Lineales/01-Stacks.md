# Stacks

Los Stacks no son estructuras nativas de JavaScript. Es decir, no existe una sintaxis específica para declararlos. Es por esto que manipulamos `arrays` para poder crear un stack.
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

Si queremos crear una clase para iniciar stacks, tendría la siguiente disposición:

```js
class Stack {
  constructor() {
    this.stack = [];
  }

  add(element) {
    this.stack.push(element);
    return this.stack;
  }

  remove() {
    this.stack.pop();
  }

  size() {
    return this.stack.length;
  }
}
```
