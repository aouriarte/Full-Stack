# Sentencias Condicionales

Es un conjunto de comandos que se ejecutan si una condición es verdadera. Javascript soporta dos:

## If ...Else

Usamos `if` para comprobar si la condición es verdadera. Se utiliza `else` para ejecutar una sentencia si la condición es falsa.
También podemos usar `else if` para evaluar múltiples condiciones.

```js
if (condición1) {
  sentencia1;
} else if (condición2) {
  sentencia2;
} else {
  setencia3;
}
```

> Para resumir esto también podemos usar el _operador ternario_.

---

## Switch

Cuando necesitamos evaluar muchas condiciones es mejor usar `switch`. Esta condicional evalúa una expresión y busca una que tenga el mismo valor con `case`, y así con los siguientes casos.

```js
switch (expresión) {
  case "valor1":
    // setencia a ejecutar si el valor1 es verdadero (true)
    break;
  case "valor2":
    // " valor2
    break;
  case "valor3":
    // " valor3
    break;
  case "valor4": // se puede incluir todos los  casos que quieras
    break;
  default:
  // setencia que se ejecuta por si acaso ninguna de las anteriores no es el valor verdadero
}
```

> `break` Es una de las declaraciones que permite que se sigan evaluando los demás casos si es que el caso donde está no es verdadeo (el valor).

---

## Valores Falsos

Se evalúan los siguiente como **falso**: `false`, `undefined`, `null`, `0`, `NaN` y `('')` cadena vacía.

Los demás valores: `true`, `(' ')`cadena vacía pero con un espacio, `1` , `[]` array, `{}` objeto, `function() {}` funciones. Son evaluados como **verdaderos** en una _sentencia condicional_.
