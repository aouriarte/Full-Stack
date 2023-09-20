# Bubble Sort

Complejidad O(n^2)
Este algoritmo ordena los números. Es el método "burbuja".
Este método compara valores continuos:

```js
[5,1,4,2,8] // nos dan un array para ordenar

/*
i siempre se comparará con j
si i > j, cambian de lugar
y siguen avanzando entre los índices
*/

// Primera pasada:                                     // en este último caso i(5) no es > que j(8), entonces finaliza.
 i->                   i                     i                     i
[5, 1, 4, 2, 8] -> [1, 5, 4, 2, 8] -> [1, 4, 5, 2, 8] -> [1, 4, 2, 5, 8] -> [1 ,4 ,2 ,5 ,8]
    j->                   j                     j                     j

// Segunda pasada: ya esta ordenado
 i
[1 ,4 ,2 ,5 ,8]
    j
// haría 2 pasadas más, ya que calcula el número de elementos del arreglo - 1
```

> Este método realiza la cantidad de pasadas según el número de elementos del arreglo. (-1)

## Código:

```js
function bubbleSort(array) {
  // crearemos un booleano para que no hagamos pasadas de más
  let swap = true; // nos avisará si hubo intecambios

  while (swap) {
    // siempre que haya intercambios
    swap = false; // lo reinicia a false
    for (let i = 0; i < array.length - 1; i++) {
      // i se para en la penúltima posición
      if (array[i] > array[i + 1]) {
        // compara valores continuos (j = i + 1)
        [array[i], array[i + 1]] = [array[i + 1], array[i]]; // los cambia de lugar
        swap = true; // avisa si entró en el if
      }
    }
  }
  return array; // retorna el array ya ordenado
}
```

> En este caso estamos realizando los pasos para que ordene los elementos de menor a mayor. Si queremos hacerlo de mayor a menor solo cambiamos la parte del `if` .
