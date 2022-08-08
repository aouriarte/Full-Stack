# KEYWORDS

## _LET_ Y _CONST_

```js
function f() {
	{
		let x;
		{ // okay, block scoped name
			const x = "sneaky";
			x = "foo";// error, const
		}
		let x = "inner"; // error, already declared in block
}
```

Las dos palabras `let` y `const` NO tienen _hoisting_ y tienen _scope_ de bloque. Esto último quiere decir que cuando declaramos en un mismo bloque un `let` y queremos modificar su contenido, la consola tirará error. Los mismo ocurre con las _constantes_.

---

## _LET_ Y _VAR_ EN LOS CICLOS FOR

```js
function crearFuncion() {
	var arreglo = [];
	for(var/let i = 0; i < 3; i++) {
		arreglo.push(function(){console.log(i);})
	}
	return arreglo;
}

var arr = crearFuncion();
 var                   let
arr[0] /*3*/          arr[0]//1
arr[1] /*3*/          arr[1]//2
arr[2] /*3*/          arr[2]//3
```

Aquí podemos ver como dependiendo en qué tipo de declaración se guardan los valores (`var` / `let`), el valor se guardará de una u otra forma.
