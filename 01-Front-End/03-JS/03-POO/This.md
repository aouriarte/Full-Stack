# This

Es una palabra clave en los objetos (clases, funciones, objetos, constructores).
Es muy útil para llamar al objeto en donde se está escribiendo.

> Es muy útil a la hora de crear **constructores**.

## **This** in objects

Veamos algunos métodos:

### Object.create

El método `create` nos permite crear un nuevo objeto a partir de uno existente como prototype del nuevo objeto creado.

```js
// creo un objeto vacío com proto
var obj1 = Object.create({});
obj1; // {}

// creo un objeto a partir de un proto de Objeto
var obj2 = Object.create(Object.prototype);
obj2; // {}

// que es lo mismo que crear un objeto vacío literal:
var obj3 = {};
```

Ejemplo:

```js
const person = {
  name: "Alexis",
  age: 20,
};

const pedro = Object.create(person);

pedro.name = "Pedro";
pedro.age = 26;

console.log(pedro); // name: 'Pedro', age: 26
```

### Object.assign

Este método nos permite agregar propiedades a un objeto pasado por parámetro.

```js
var animal = {};

// no hace falta guardar el resultado porque los objetos se pasan por 'referencia'
Object.assign(animal, { especie: "perro", edad: "5meses" });

animal.especie; // 'perro'
```

---

## **This** in functions

Llama al objeto contexto en el cual se está ejecutando el código actual. Vimos ejemplo en los **_objects_**.
En las funciones flecha el `this` hace referencia al "windown". Por ello tenemos métodos que nos permitirán **elegir a nosotros** que código se llamará:

### Bind

_Asociar, unir_, Crea una nueva función a partir de la función que se llama en su valor 'this'.

```js
var persona = {
  nombre: "Alexis",
  apellido: "Uriarte",
};

var logNombre = function () {
  console.log(this.nombre);
};

var logNombrePersona = logNombre.bind(persona); // llama a la función 'logNombre'
// function(){
//  console.log(persona.nombre);
// }

// el primer parámetro de bind es 'this', lo que se llama.
logNombrePersona(); // 'Alexis'
```

También nos permite dejar _parámetros_ fijos

```js
function multiplica(a, b) {
  return a * b;
}

// el primer parámetro de BIND es a lo que haga referencia el 'this'
// luego en orden sus parámetros
var multiplicarPor2 = multiplica.bind(null, 2); // 'null' no torna nada
// function multilplica(2, b) { --> '2' se convierte en 'a', en el primer parámetro.
//  return 2 * b;
// }

multiplicaPor2(3); // 6
multiplicaPor2(4); // 8
```

---

### Call

Es lo mismo que 'BIND' pero no crea una nueva función, osea no retiene esa función como lo hace _bind_ sino que la ejecuta ahí mismo.

```js
var persona = {
  nombre: 'Alexis',
  apellido: 'Uriarte',
}

var logNombre = function() {
  console.log(this.nombre);
}

// el primer parámetro de call es 'this'
logNombre.call(persona); // ejecuta acá mismo console.log(persona.nombre)

// call hace lo mismo que BIND, solo que invoca la función, no devuelve nada.
// también bindea argumentos:

var logNombre = function (arg1, arg2) {
  console.log(arg1 +' '+ this.nombre +' '+ arg2),
}

logNombre.call(persona, 'Hola', ', Cómo estás?'); // Hola Alexis, Cómo estás?
```

---

### Apply

Es igual a _call_, solo que el segundo argumento es un arreglo.

```js
var logNombre = function (arg1, arg2) {
  console.log(arg1 + " " + this.nombre + " " + arg2);
};

logNombre.apply(persona, ["Hola", ", Cómo estás?"]); // Hola Alexis, Cómo estás?
```
