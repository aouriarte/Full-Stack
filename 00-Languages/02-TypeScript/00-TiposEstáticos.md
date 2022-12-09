# Tipos Estáticos

TypeScript nos ayuda a controlar el tipo de dato que va almacenar a nuestras variables:

```ts
let palabra = "Hola";
palabra = 5; // JavaScript me dejaría hacer esto

let numero: number = 5;
numero = "Hola"; // El tipo 'string' no se puede asignar al tipo 'number'
```

Podemos asignar tipos de datos [primitivos](../01-JavaScript/01-BASIC/02-TiposDatos.md):

```ts
let texto: string = "palabra";
let numero: number = 21;
let respuesta: boolean = true;
let vacio: null = null;
let indefinido: undefined = undefined;
```

También podemos crear nuestro propios **"tipos de datos"**.
Creamos nuestro nuevo tipo `Operations` usando la palabra clave `type` ,lo hacemos tal cual creamos una variable y asignamos el o los valores a ese tipo.

```ts
type Operations = "suma" | "resta" | "multiplicación" | "división";

const calculator = (a: number, b: number, op: Operations) => {
  if (op === "suma") return a + b;
  if (op === "resta") return a - b;
  if (op === "multiplicación") return a * b;
  if (op === "división") {
    else if (a < b) return `No se puede dividir ${a} entre ${b}`;
    else if (a === 0) return `No se puede dividir 0 entre ${b}`;
    return a / b;
  }
};

console.log(calculator(14, 7, "división")); // 2
console.log(calculator(14, 7, "add")); // No se puede asignar un argumento de tipo ""add"" al parámetro de tipo "Operations".
```

> Aquí vemos que al pasar "add" como parámetro de nuestra función nos dirá que ese argumento no existe en nuestro tipo "Operations", esto es lo mismo que ocurrió anteriormente al intentar asignar un dato de tipo diferente a nuestra variable.

Además otro beneficio es que podemos definir el tipo de dato que nuestra función va a devolver.

Podemos hacerlo así, creando nuevamente nuestro porpio tipo:

```ts
type Operations = "suma" | "resta" | "multiplicación" | "división";
type Result = number | string;

const calculator = (a: number, b: number, op: Operations): Result => {
  if (op === "suma") return a + b;
  if (op === "resta") return a - b;
  if (op === "multiplicación") return a * b;
  if (op === "división") {
    if (a < b) return `No se puede dividir ${a} entre ${b}`;
    if (a === 0) return `No se puede dividir 0 entre ${b}`;
    return a / b;
  }
};
```

o ponerlo explícitamente al final:

```ts
type Operations = "suma" | "resta" | "multiplicación" | "división";

const calculator = (a: number, b: number, op: Operations): number | string => {
  if (op === "suma") return a + b;
  if (op === "resta") return a - b;
  if (op === "multiplicación") return a * b;
  if (op === "división") {
    if (a < b) return `No se puede dividir ${a} entre ${b}`;
    if (a === 0) return `No se puede dividir 0 entre ${b}`;
    return a / b;
  }
};
```

### Desventajas

La compliación que hay si es que compilamos la operación pasandole parámetros incorrectos a la función, ese error que nos tirará no lo podrá ver el usuario, por lo que si estamos trabajando en nuestra App no sabremos donde está el error hasta abrirlo. Hay muchas maneras de arreglar ello:

```ts
type Operations = "suma" | "resta" | "multiplicación" | "división";

const calculator = (a: number, b: number, op: Operations): number => {
  if (op === "suma") return a + b;
  if (op === "resta") return a - b;
  if (op === "multiplicación") return a * b;
  if (op === "división") {
    if (a < b) throw new Error(`No se puede dividir ${a} entre ${b}`);
    if (a === 0) throw new Error(`No se puede dividir 0 entre ${b}`);
    return a / b;
  }

  throw new Error(`La ${op} no está definida`);
};
```
