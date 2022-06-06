# LinkedList

Es un tipo de lista de _elementos_ en los que cada elemento tiene almacenada la _referencia al siguiente_ elemento, de tal forma que si queremos acceder a un elemento en particular tenemos que empezar por el primer elemento, para recorrer uno a uno.
Pueden ser _simplemente enlazadas_, _dobles_ o _múltiples_ según las restricciones que tengan sus _referencias_(next).

## Estructura

No son estructuras nativas en Javascript por ello tenemos que definirlas nosotros mismos:

```js
function LinkedList() {
  this.head = null; // cabeza de lista
  this._length = 0; // tamaño de lista (opcional)
}

function Node(value) {
  // Los elementos de la lista
  this.value = value; // el valor
  this.next = null; // la referencia añ siguiente elemento
}
```

```js
Cabeza (head)
  |
  v               current => apuntador de los nodos, para recorrer la lista

 ----------       ----------       ----------       --------
|valor|    |     |valor|    |     |valor|    |     |        |
| 4   |  ------> | 9   |  ------> | 13  |  ------> | null   |
|     |sgte|     |     |sgte|     |     |sgte|     |        |
 ----------       ----------       ----------       --------
   Nodo              Nodo             Nodo             Nodo
```

## Métodos

### AGREGAR NODOS

```js
LinkedList.prototype.add = function (value) {
  var nuevoNodo = new Node(value);
  var current = this.head; // recorrerá la lista desde la cabeza

  // AGREGAR NODO COMO CABEZA
  if (!this.head) {
    // current === null, verificar si la cabeza de lista está vacía
    this.head = nuevoNodo; // agrega el nodo valor ahí
  }
  // AGREGAR NODO DESPUÉS DE LA CABEZA
  else {
    while (current.next) {
      // current.next !== null
      current = current.next; // sigue avazando hasta que esté vacío
    }
    current.next = nuevoNodo; // cuando esté vacío, agrega el valor ahí
  }
};
```

---

### ELIMINAR NODOS

```js
LinkedList.prototype.remove = function () {
  var current = this.head; // recorrer

  // LISTA VACÍA
  if (!this.head) return null; // === null

  // SI SOLO HAY UN NODO
  if (!this.head.next) {
    // === null
    let eliminado = this.head; // this.head.value
    this.head = null; // elimina la cabeza de lista
    return eliminado.value; // retornar el valor
  }

  // SI HAY DOS O MÁS NODOS
  while (current.next.next) {
    // se para en el nodo ante-penúltimo
    current = current.next; // seguirá avanzando
  }
  let eliminado = current.next.value; // guardamos el valor de ese nodo
  current.next = null; // el sgte nodo en donde estoy, lo elimina
  return eliminado;
};
```

---

### BUSCAR VALORES

```js
LinkedList.prototype.search = function (arg) {
  var current = this.head;

  // LISTA VACÍA
  if (!this.head) return null;

  // HAY NODOS
  while (current) {
    if (typeof arg === "function") {
      // si es una función
      if (arg(current.value)) {
        // lo encontré
        return current.value;
      }
    } else if (current.value === arg) {
      // si donde está es el valor
      return current.value;
    }
    current = current.next; // sigue buscando
  }

  return null; // no encuentra lo buscado
};
```

---

### IMPRIMIR VALORES DE CADA NODO

```js
List.prototype.getAll = function () {
  var current = this.head;

  // LISTA VACÍA
  if (!current) {
    console.log("La lista esta vacia!");
    return;
  }

  // CONTENIDO DE LISTA
  while (current) {
    // recorrido
    console.log(current.data); // cada vez que pase por un nodo, imprimirá el valor
    current = current.next;
  }

  return;
};
```
