# Trees

Existen muchos tipos de _Árboles_. Veremos los _Binarios_. Son listas simplemente enlazadas, con la diferencia que puedan conectar con ningún, 1 o 2 nodos.

## Estructura

- _*Nodo padre/Nodo raíz:*_ es el primer nodo que se crea.
- _*Nodo hijo:*_ hace referencia a los nodos que se descienden de otros.
- _*Nodos hermanos:*_ son aquellos que están en el mismo nivel.
- _*Nodo hoja:*_ son los nodos que no tienen hijos.

```js

                  Root (raíz)
                    -------
         Nodo -->  |   A   | ------------------------------------- Level 0
                    -------
                   ´       `
                  ´         `
                 v            v
          -------              -------
         |   B   |(nodo padre)|   C   | -------------------------- Level 1
          -------              -------
          ´                  ´     `
         ´                  ´       `
        v                  v         v
  -------                -------      -------
 |   C   | (nodo hoja)  |   D   |    |   E   | (hermanos) ---------- Level 2
  -------                -------      -------
                        (nodo hijo)
```

> Por cada nuevo nodo se forma un _sub-árbol_.

---

## Tipos

Dentro de los árboles binarios existen muchos otros tipos de árboles:

### Binary Search Tree

Los _Árboles Binarios de Búsqueda_ tienen la diferencia de que estos son ordenados.
La forma de orden de estos árboles es que, del _lado izquierdo_ van a tener siempre un valor de referencia _menor_, y del _lado derecho_ un valor _mayor_.

```js
                    ______|15|______
               __|9|__            __|20|__
            |6|      |14|      |17|       |64|
                  |13|                 |26|  |72|
```

A su vez dentro de estos árboles existen:

- **AVL:** Son los _auto-balanceados_. Quiere decir que, entre los nodos de mayor nivel, _difieren entre 0 y 1_ nivel con otras ramificaciones:

```js
           __|3|__                       ______|3|______
       _|2|_      |0|                _|2|_             _|2|_
    |1|     |0|                   |1|     |0|       |1|     |1|
  |0| |0|                       |0| |0|     |0|   |0| |0| |0| |0|
```

> El de la izquierda es _no balanceado_. El de la derecha es _balanceado_.

- **MAX HEAP:** Estos árboles tienen la particularidad de que los valores se distribuyen de _arriba (mayores)_ hacia _abajo (menores)_:

```js
                    ______|100|______
              __|19|__             __|36|__
          |17|        |3|      |25|        |1|
        |2|  |7|
```

> En el caso de que esto fuera al revez (que los números _menores van de arriba hacia abajo_), este árbol se llamaría **MIN HEAP**.

---

## Recorridos
