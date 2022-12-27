# Quick Sort

Complejidad O(n log n), en el peor de los casos sería O(n^n)
Método de ordenamiento rápido.

```js
[5, 1, 4, 2, 8][ // nos dan un array para ordenar
  /* Elegiremos un elemento a ordenar, llamado PIVOT
(puede ser cualquiera, el final, el principio, el medio) */

  (5, 1, 4, 2, 8)
][/* Todos los demás elementos serán ordenados según el pivot: // 5
Los menores a su izquierda y los mayores a su derecha. 
Si un elemento es igual al Pivot, da igual a que lado se manda. */

// Primera vez:
5][/*menores*/ (1, 2, 4)][8] /*mayores*/[ //PIVOT
  /* Así de formarán sub-listas de los elementos que se van ordenando. 
Haremos esto mientras los array contengan más de un elemento, lo haremos con recursión */

  // Segunda vez: (en este caso quedaron ordenados)
  (1, 2, 4, 5, 8)
];
```

## Código:

```js
function quickSort(array) {
  if (array.length <= 1) return array; // array = [] o [1]

  let pivot = array[0]; // primer elemento
  let menores = [];
  let mayores = [];

  for (var i = 1; i < array.length; i++) {
    // comienza en segunda posición
    if (array[i] < pivot) {
      menores.push(array[i]);
    } else {
      mayores.push(array[i]);
    }
  }
  return [].concat(quickSort(menores), pivot, quickSort(mayores)); // manera de unir arrays también: return quickSort(left).concat(pivot, quickSort(right));
}
```

> Para ordenarlo de mayor a menor, podemos cambiar el `if` a `>` o cambiar el orden en que se concatenan los array.
