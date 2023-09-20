# Insertion Sort

Complejidad O(n^2)
Va ordenando a medida que recorre. Compara valores hacia la izquierda.

```js
[5, 1, 4, 2, 8]; // nos dan un array para ordenar

/*
i = sacará el valor que se va a intercambiar (funcionará como la garra)
*/
     i                i                i                i
  [5,1,4,2,8] -> [1,5,4,2,8] -> [1,4,5,2,8] -> [1,2,4,5,8]
   j                j                j                j
/*
siempre corre hacia la izq. <--j y siempre se resetea a i-1
*/
```

## Código:

```js
function insertionSort(array) {
  for (let i = 1; i < array.length; i++) {
    let j = i - 1;
    let garra = array[i];
    while (j >= 0 && array[j] > garra) {
      // que j no se pare antes de la posición 0 en el array y sea mayor al valor que tiene i
      array[j + 1] = array[j]; // pisa al sgte por el anterior
      j--; // y j se me mueve a la posición anterior
    }
    array[j + 1] = garra; // suelta el valor una posición después del valor en donde quedó
  }
  return array;
}
```

> cambiamos en el while `j >= 0 && array[j] < garra` para que sea de mayor a menor.
