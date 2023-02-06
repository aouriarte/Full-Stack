# Object Literals

```js
var apellido = "Uriarte";

var objeto = {
	saludo: "hola",
	saludar() {console.log("buen día"),
	apellido,
	["prop" + "dinámica"]: 10
};
```

Los objetos tienen una estructura de _clave-valor_. Cuando queremos que una de las propiedades sea un método, no hace falta pasarle una clave.

A su vez, cuando queremos insertar una variable en el objeto, solo basta pasarle como parámetro el nombre de la variable.

Por último, podemos pasar como nombre de una propiedad a una operación lógica. Esta operación lógica debe ir entre **corchetes**. En este caso, el nombre de la propiedad es _“propdinámica”_ ya que es una concatenación de strings.
