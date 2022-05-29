# Queues

Las _colas_ tampoco son nativas de JavaScript, por lo que también tendremos que simularlas con los `arrays` . Se manejan con FIFO (First In, Firt Out) el primero en llegar el primero en irse.

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

Si queremos crear una clase de Queue, se dispondría de la siguiente manera:

```js
class Queue {
  constructor() {
    this.queue = [];
  }

  enqueue(element) {
    this.queue.push(element);
    return this.queue;
  }

  dequeue() {
    this.queue.shift();
  }

  size() {
    return this.queue.length;
  }
}
```
