# TypeScript

TypeScript es un lenguaje de código abierto desarrollado por Microsoft. Se trata de un _supraconjunto_ de [JavaScript](../01-JavaScript/JavaScript.md).

Quiere decir que **aborda las limitaciones de JavaScript** sin poner en peligro la propuesta de valor clave de JavaScript: la capacidad de ejecutar el código en cualquier lugar y en cualquier plataforma, explorador o host.

## Sugerencias de escritura

La característica principal de TypeScript es su sistema de tipos. En TypeScript, puede identificar el tipo de datos de una variable o un parámetro mediante una _sugerencia de tipo_. También implementa algunas características, como los _tipos estáticos_.

## Otras características

- Interfaces
- Espacios de nombres
- Genéricos
- Clases abstractas
- Modificadores de datos
- Valores opcionales
- Sobrecarga de funciones
- Elementos Decorator
- Tipos de utilidad
- Palabra clave readonly

## Complicación de TypeScript

Para transformar código TypeScript en JavaScript, use el compilador de TypeScript o un transpilador compatible con TypeScript, como [Babel](https://babeljs.io), [swc](https://swc.rs/docs/getting-started) o [Sucrase](https://github.com/alangpierce/sucrase). Esto genera un archivo JavaScript limpio que puede ejecutar en las páginas web y que es compatible con los exploradores.

## Tipos Estáticos

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
