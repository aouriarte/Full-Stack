# Template Strings

```js
var b = "hola
cómo estás"
var a = "Hola \n cómo estás"
```

> Existen algunas restricciones en JavaScript. Por ejemplo, solo se puede hacer un _new line_ en el medio de un string. `\n` sirve para hacer este cometido.

```js
var z = `Hola cómo estás`;

var q = `Hola ${name} cómo estás? Hoy es ${(() => 10 + 6)()} de febrero`;
// Hola Juan como estas? Hoy es 16 de febrero.
```

- Las comillas reversas ` ` (alt + 96) son **literal strings**.

- La estructura `${coso}` sólo sirve cuando se lo utiliza entre comillas invertidas.
