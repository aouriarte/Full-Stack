# Herencia Clásica

En el paradigma de _Programación Orientada a Objetos_ un tema muy importante es la **Herencia** y **Polimorfismo**.

- Herencia: Nos referimos a la capacidad de un constructor de _heredar_ propiedades y métodos de otro constructor, así como un Gato es Mamífero antes que Gato, y hereda sus 'propiedades' (nace, se reproduce y muere).

- Polimorfismo: Capacidad de que objetos distintos puedan responder a un mismo llamado de acuerdo a su propia naturaleza.

## Herencia en Javascript

A diferencia de la herencia clásica, en JS nos manejamos con prototipos, que tomarán los métodos por sus 'padres' mediante la `Prototype Chain` .

> Podemos generar nuestros propios constructores de los cuales heredar:

```js
function Persona(nombre, apellido, ciudad) {
  this.nombre = nombre;
  this.apellido = apellido;
  this.ciudad = ciudad;
}

Persona.prototype.saludar = function () {
  console.log("Soy " + this.nombre + " de " + this.ciudad);
};

var Alexis = new Persona("Alexis", "Uriarte", "Lima");

Alexis.saludar(); // 'Soy Alexis de Lima'
```

> Ahora todo Alumno de Henry antes de Alumno es una Persona, así que podríamos decir que un Alumnno hereda las propiedades de ser Persona:

```js
function Alumno(nombre, apellido, ciudad, curso) {
  // podría copiar las mismas propiedades de Persona acá dentro
  this.nombre = nombre;
  this.apellido = apellido;
  this.ciudad = ciudad;
  this.curso = curso;
}

var Juan = new Alumno("Juan", "Pérez", "Buenos Aires", "Javasript");
```
