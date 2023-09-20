# Recursión

Es una función que se llama así misma. Funciona como una especie de bucle. Es muy útil cuando queremos realizar una misma tarea siempre o muchas veces.

**Características:**

- La función debe tener una (o más) sentencia base. Osea casos de corte.
- La función debe llamarse a sí misma.
- El argumento cuando la función se vuelve a invocar debe ser distinto del argumento de la función padre.

```js
// hallar el 'factorial' de manera lógica:
// 4! = 4x3x2x1 = 4x3!
// 3! = 3x2x1 = 3x2!
// 2! = 2x1!
// así cada uno.

// intentaremos hallar el 'factorial' de un número en código:
function factorial(num) {
  if (num === 0 || num === 1) return 1; // casos base
  if (num < 0) return 0; // casos base
  return num * factorial(num - 1); // aquí la función se llama a sí misma
}

/* Proceso de ejecución:

factorial(2) = 2 * factorial(1) --> retornará 1
factorial(3) = 3 * factorial(2) --> así cada ejecución, hasta que devuelva un valor.
factorial(4) = 4 * factorial(3) --> ahora se necesita ejecutar esta función antes de multiplicarla y se agrega a la pila de ejecución: FIFO (First In, Firs Out)

factorial(2) = 2 * 1 // al ya tener el valor, se puede multiplicar.
factorial(3) = 3 * 2 // cada uno comienza a retornar su valor
factorial(4) = 4 * 6 // y se va saliendo del proceso de ejecución

factorial(4); // 26
*/
```
