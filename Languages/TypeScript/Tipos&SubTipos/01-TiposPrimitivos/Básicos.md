# Tipos primitivos

## **string**

También usa comillas dobles (`"`) o comillas simples (`'`).

```ts
let s: string;
let empty = "";
let abc = "abc";
```

En TypeScript, también podemos usar los Template String o Cadena de platilla `${expr}`.

```ts
let firstName: string = "Mateo";
let sentence: string = `My name is ${firstName}. I am new to TypeScript.`;
console.log(sentence); // My name is Mateo. I am new to TypeScript.
```

## **number** y **BigInteger**

Son valores de número de punto flotante o BigIntegers. Estos números de punto flotante obtienen el tipo `number`, mientras que los valores BigIntegers obtiene el tipo `bigint`. Además de los literales hexadecimales y decimales, TypeScript también admite los literales binarios y octales introducidos en ECMAScript 2015.

```ts
let x: number;
let y = 0;
let z: number = 123.456;
let big: bigint = 100n;
```

## **boolean**

Igual que JS.

```ts
let flag: boolean;
let yes = true;
let no = false;
```

## **null** y **undefined**

Son subtipos de todos los demás tipos. No es posible hacer referencia explícita a estos tipos. Por ello se hace referencia mediante los literales `undefined` y `null`.

```ts
let vacio: null = null;
let indefinido: undefined = undefined;
```

## **void**

El tipo `void` existe únicamente para indicar la ausencia de un valor, como en una función sin ningún valor devuelto.
