# Enum

Ofrecen una manera sencilla de trabajar con conjuntos de **constantes** relacionadas. Las enumeraciones se tratan como tipos de datos y se pueden usar a fin de crear conjuntos de constantes para su uso con variables y propiedades. Permiten especificar una lista de opciones disponibles.

De forma predeterminada, los valores enum comienzan con un valor de 0.

```ts
enum DiasDeSemana {
  Lunes, // 0
  Martes, // 1
  Miercoles, // 2
  Jueves, // 3
  Viernes, // 4
  Sabado, // 5
  Domingo, // 6
}

let dia: DiasDeSemana = DiasDeSemana.Jueves;
console.log(dia); // 3
```

> pero podemos cambiar el valor en el que empiecen:

```ts
enum DiasDeSemana {
  Lunes = 1, // 1
  Martes, // 2
  Miercoles, // 3
  Jueves, // 4
  Viernes, // 5
  Sabado, // 6
  Domingo, // 7
}

let dia: DiasDeSemana = 3;
console.log(DiasDeSemana[dia]); // Miercoles
```
