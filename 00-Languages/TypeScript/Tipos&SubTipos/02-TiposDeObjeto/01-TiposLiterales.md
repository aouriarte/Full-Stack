# Tipos Literales

Un literal es un subtipo más concreto de un tipo colectivo.

Hay tres conjuntos de tipos literales disponibles en TypeScript: `string`, `number` y `boolean`.

```ts
type testResult = "pass" | "fail" | "incomplete";
let myResult: testResult;
myResult = "incomplete"; //* Valid
myResult = "pass"; //* Valid
myResult = "failure"; //* Invalid
```

> Es como una manera de crear nuestros propios tipos para especificar un valor exacto que debe tener una cadena, un número o un valor booleano.
