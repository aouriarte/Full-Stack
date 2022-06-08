# Algoritmos

Es un conjunto de instrucciones o reglas bien definidas, ordenadas y finitas para realizar una tarea. O sea, pasos a seguir.

## Características

- **Resuelve un problema:** este es el objetivo principal del algoritmo, fue diseñado para eso. Si no cumple el objetivo, no sirve para nada.
- **Debe ser comprensible:** el mejor algoritmo del mundo no te va a servir si es demasiado complicado de implementar.
- **Hacerlo eficientemente:** no sólo queremos tener la respuesta perfecta (o la más cercana), si no que también queremos que lo haga usando la menor cantidad de recursos posibles.

### EFICIENCIA

¿Cómo la medimos?

- **Tiempo:** no depende solamente de que el algoritmo sea eficiente. También depende de la computadora que usemos, el procesador, la consola, etc.
- **Espacio:** espacio de memoria que requiere.
- **Otros Recursos:** red, gráficos, hardware, etc.

### COMPLEJIDAD

¿Por qué es importante medir la complejidad de un algoritmo?

- Primero, porque nos permite **_predecir su comportamiento_**. Si estamos en frente de un algoritmo muy complejo, puede que ocupe todo el procesador de nuestra PC y esta se rompa.

- Segundo, porque nos permite **_compararlo_**. Si podemos saber objetivamente qué tan complejo es, cuando lo comparemos con otros podremos ver cuál es más eficiente.

Este es un ejemplo de dos algoritmos (uno eficiente y otro ineficiente) que buscan un número entre muchos:

```js
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10] // Se tiene que adivinar un número del 1 al 10
				        ^^^

E1 O(N) /* lineal */      E2 LOG(N) /* algorítmica */
1                         5 //es + o - que 5? -----------  +
2                         8 //es + o - que 8? -----------  +
3                         9 :D
4                         // este hizo menos pasos
5
6
7
8
9:D //este realizó más pasos
```

> La Notación **O** grande (Big-O) sirve para medir la complejidad de un algoritmo

```js
function(arr) {
	console.log("Hola");   // 1 operación
	console.log("Chau");   // 1 operación
	let acu = 2 + 3;       // 1 operación
	return array[0];       // 1 operación
}
```

En este caso, indistintamente de la longitud del arreglo que pasemos por parámetro, este algoritmo siempre hará 4 operaciones. Ni más ni menos. A esto se lo conoce como **O(1)** (constante), que es el mejor de los casos en el rendimiento de un algoritmo.

#### TIPOS DE Big-O Notation:

```js
// mejor rendimiento v
- O(1) -> constante.
- O(log n) -> logarítmica.
- O(n) -> lineal.
- O(n log n) -> algorítmica
// peor de los casos v
- O(n ^ 2) -> cuadrática.
- O(2 ^ n) -> exponencial.
- O(n!) -> explosión combinatoria
```

A medida que aumenta la complejidad, el tiempo necesario para completar la tarea crece mucho, pudiendo llegar a aumentar enormemente en algunos casos en cuanto hay más datos a manejar. Creo que verlo gráficamente es la mejor manera de darse cuenta de su importancia.
