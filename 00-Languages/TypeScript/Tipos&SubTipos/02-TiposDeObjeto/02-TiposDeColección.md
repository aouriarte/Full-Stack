# Tipos de colección

## Matrices

Las matrices se pueden escribir de dos maneras:

- En la primera usamos el tipo de elemento + `[]`.

```ts
let list: number[] = [1, 2, 3];
```

- En el segundo caso usamos un tipo `Array` genérico con la sintaxis `Array<type>`.

```ts
let list: Array<number> = [1, 2, 3];
```

---

## Tuplas

Tener una matriz de los mismos tipos de valor es útil, pero a veces tiene una matriz que contiene valores de tipos mixtos. Para ese propósito, TypeScript proporciona el tipo de tupla.

Para declarar una tupla, use la sintaxis `variableName: [type, type, ...]`.

```ts
let person1: [string, number] = ["Marcia", 35];
let person2: [string, number] = [35, "Marcia"]; // El tipo "number" no se puede asignar al tipo "string"
```

> El orden de los valores deben coincidir con el orden de los tipos.
