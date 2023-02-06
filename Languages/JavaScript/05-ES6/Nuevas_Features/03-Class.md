# CLASS

Las **_clases_** sólo cambiaron la sintaxis de las _funciones constructoras_.

```js
/*
function Persona(nombre, edad) {
	this.nombre = nombre;
	this.edad = edad;
}
*/
class Persona {
  constructor(nombre, edad) {
    this.nombre = nombre;
    this.edad = edad;
  }
};

var newPersona = new Persona(nombre, edad);
```

En este ejemplo vemos la forma más básica de una clase, donde solo tiene dos atributos.

```js
class Persona {
  constructor(nombre, edad) {
    this.nombre = nombre;
    this.edad = edad;
  }
};

class OtraPersona extends Persona {
  constructor(nombre, edad, empleo) {
    super(nombre, edad);
    this.empleo = empleo;
  }

  metodo1() {}

  metodo2() {}
};
```

En este ejemplo vemos la propiedad **extend** de las clases. Podemos heredar en una nueva clase los atributos con la palabra clave **super**. De por sí, la extensión también hereda los métodos:
