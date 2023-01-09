# Tipos Estáticos

TypeScript nos ayuda a controlar el tipo de dato que va almacenar a nuestras variables:

```ts
let palabra = "Hola";
palabra = 5; // JavaScript me dejaría hacer esto

let numero: number = 5;
numero = "Hola"; // El tipo 'string' no se puede asignar al tipo 'number'
```

Los tipos de datos pueden ser implícitos o explícitos:

```ts
let x: number; //* Explicitly declares x as a number type
// x = 'one'   // el tipo 'string no se puede asignar al tipo 'number

let y = 1; //* Implicitly declares y as a number type
// y = 'hola' // el tipo 'string no se puede asignar al tipo 'number

let z; //* Declares z without initializing it
z = "good"; // así no debería hacerlo
z = true;
```
