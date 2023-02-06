# Selection Sort

Complejidad O(n^2)
Selecciona el valor mínimo y lo compara con los valores siguientes.

```js
[5,1,4,2,8] // nos dan un array para ordenar

/*
i se queda fijo hasta que min se ordene.
Al empezar uuna nueva vuelta:
empieza min = i, si j < i, será min = j
Sino:
j sigue avanzando y min se compara con él
*/

 i                  i
[5, 1, 4, 2, 8] -> [5, 1, 4, 2, 8] (min = 1, se compara con los demás j) ---> [1, 5, 4, 2, 8]
    j                     j++
min                   min

// cuando el valor de min se ordena, i cambia al valor siguiente
// '--->' representa las vueltas hechas

    i                  i                  i
[1, 5, 4, 2, 8] -> [1, 5, 4, 2, 8] -> [1, 5, 4, 2, 8] -> [1, 2, 5, 4, 8] --->
       j                     j                     j
   min                   min                   min

// cuando termina de recorrer, min se ordena en donde está i

       i                  i
[1, 2, 5, 4, 8] -> [1, 2, 5, 4, 8] -> [1, 2, 4, 5, 8] ---> Terminó
          j                     j
      min                   min
```

## Código:

```js
function selectionSort(array) {
  for (let i = 0; i < array.length; i++) {
    let min = i; // empieza en i
    for (let j = i + 1; j < array.length; j++) {
      // j sigue recorriendo
      if (array[j] < array[min]) {
        min = j;
      }
    } // no entró en el for(j)
    let aux = array[i]; // se guarda el valor de i
    array[i] = array[min]; // donde estaba i toma el valor del min
    array[min] = aux; // min comienza en i nuevamente
  }
  return array;
}
```

> Podemos cambiar el método de ordenar de menor a mayor por al revés, cambiando el `if` .
