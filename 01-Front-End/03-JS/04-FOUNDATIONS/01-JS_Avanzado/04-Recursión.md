## Recursión

Es una función que se llama así misma hasta cortar con su caso base, osea su valor de retorno. Como una especie de bucle. Es muy útil cuando queremos realizar una misma tarea siempre o muchas veces.

```js
// hallar el 'factorial' de manera lógica:
// 4! = 4x3x2x1 = 4x3!
// 3! = 3x2x1 = 3x2!
// 2! = 2x1!
// así cada uno

// intentaremos hallar el 'factorial' de un número en código:
function factorialRec(num) {
  if (num === 0 || num === 1) return 1;
  if (num < 0) return 0;

  return num * factorialRec(num - 1); // aquí la función se llama a sí misma
}

/* Proceso de ejecución:

factorialRec(2) = 2 * factorialRec(1) --> retornará 1
factorialRec(3) = 3 * factorialRec(2) --> así cada ejecución, hasta que devuelva un valor.
factorialRec(4) = 4 * factorialRec(3) --> ahora se necesita ejecutar esta función antes de multiplicarla y se agrega a la pila de ejecución: FIFO (First In, Firs Out)

factorialRec(2) = 2 * 1 // al ya tener el valor, se puede multiplicar.
factorialRec(3) = 3 * 2 // cada uno comienza a retornar su valor
factorialRec(4) = 4 * 6 // y se va saliendo del proceso de ejecución

factorialRec(4); // 26
*/
```
