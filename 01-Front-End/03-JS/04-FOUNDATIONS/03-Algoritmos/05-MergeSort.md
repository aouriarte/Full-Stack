# Merge Sort

Complejidad O(n log n).
Divide el conjunto en dos grupos iguales. Ordena recursivamente los dos grupos. Junta los grupos ordenados.

```js
// Primero: recursión para partir a la mitad siempre que haya más de un elemento:
            [5,1,4,2,8] // nos dan un array para ordenar
     [5,1,4]           [2,8]
  [5]       [1,4]   [2]     [8]
         [1]     [4]

// Segundo: recursión para unir de forma ordenada
// comparando cada elemento de cada arreglo.
[1,2,4,5,8]
```

## Código:

```js
function mergeSort(array) { 
  if (array.length <= 1) return array; // array = [] o [1]

  let mid = Math.floor(array.length/2); // corta a la mitad
  let left = array.slice(0, mid); // copia del inicio a la mitad
  let right = array.slice(mid); // de la mitad al final

  return merge(mergeSort(left), mergeSort(right)); // recursión
  
};

function merge(left, right){ // función que se usa como la recursión
  let i = 0;
  let d = 0;
  let arrOrdenado = [];

  while(i < left.length && d < right.length){
    if(left[i] < right[d]){
      arrOrdenado.push(left[i]);
      i++;
    }
    else {
      arrOrdenado.push(right[d]);
      d++;
    }
  }
  return arrOrdenado.concat(left.slice(i)).concat(right.slice(d)); // concatena si sobró de ambos
};
```