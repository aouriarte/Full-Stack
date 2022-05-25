# Constructor

Son útiles para crear muchos objetos que comparten algunas de las mismas propiedades y métodos (como los usuarios en un sitio web).

Se instacia de manera _pseudo clásica_, usando la keyword `new` , y puede tomar argumentos. (Se crea).

```js
function Gato(nombre) {
  // el nuevo operador crea un objeto, "this"
  this.nombre = nombre;
  this.maullar = function () {
    return "Mi nombre es " + this.nombre + " ... Meow!";
  };
  // devuelve el objeto "this"
}

const sam = new Gato("Sam");
const kitty = new Gato("Kitty");
console.log(sam.maullar()); // 'Mi nombre es Sam ... Meow!'
console.log(kitty.maullar()); // 'Mi nombre es Kitty ... Meow!
```

> La convención de usar clases consiste en dar un nombre con _MAYÚSCULA_ al nombre de todo lo que se puede instanciar con la palabra clave `new` .

## Prototype

Es la forma de establecer un método a la vez y dar acceso a cada objeto de esa clase a esos métodos.
Cada clase tiene esta propiedad que nos permite luego establecer métodos:

```js
function Usuario(nombre, edad) {
    this.nombre = nombre;
    this.edad = edad;
}

Usuario.prototype.saludo = function(){
    return 'Me llamo ' + this.nombre + ' y tengo ' this.edad + '.';
}

let juan = new Usuario('Juan', '25');
let alex = new Usuario('Alex', '20');

console.log(juan.saludo()); // Me llamo Juan y tengo 25.
console.log(alex.saludo()); // Me llamo Alex y tengo 20.
```

---

## Set 

Es parecido a los arreglos, solo que crea un nuevo _objeto_ sin que se repita sus valores. Es un constructor. Es para cualquier tipo de dato.

```js
var arreglo = [1,2,3,4,,1,3,1,7,5]
var set1 = new Set(arreglo)
console.log(set1); // Set {1,2,3,4,7,5} 
```