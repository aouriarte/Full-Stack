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
