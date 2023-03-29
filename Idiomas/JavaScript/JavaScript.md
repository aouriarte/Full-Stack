# JavaScript

Es un lenguaje de **_scripting_** multiplataforma y orientada a objetos.

## Isomorfismo

Es el único lenguaje capaz de ejecutarse en las 3 capas de una aplicación:

1. **Frontend** (con JavaScript).
2. **Backend** (con Node.js).
3. Persistencia de Datos (con MongoDB, Couch DB, Firebase, etc).

Con JavaScript puedes:

- Diseño y Desarrollo Web.
- Hacer Videojuegos.
- Experiencias 3D, Realidad Aumentada, Realidad Virtual.
- Controlar Hardaware (drones, robots, electrodomésticos, wearables, etc).
- Aplicaciones Híbridas y Móviles.
- Aprendizaje Automático.
- Etc.

## Características

- Lenguaje de Alto Nivel.
- Interpretado.
- Dinámico.
- Débilmente Tipado.
- Multiparadigma.
- Sensible a MAYÚSCULAS y minúsculas.
- No necesitas los puntos y comas al final de cada línea.

## Palabras Reservadas (**Keywords**)

```js
A: abstract
B: boolean, break, byte
C: case, catch, char, class, const, continue
D: debugger, default, delete, do, double
E: else, enum, export, extends
F: false, final, finally, float, for, function
G: goto
I: if, implements, import, in, instanceof, int, interface
L: let, long
N: native, new, null
P: package, private, protected, public
R: return
S: short, static, super, switch, synchronized
T: this, throw, throws, transient, true, try, typeof
V: var, volatile, void
W: while, with
```

## Escritura de código

Es como la gramática de la programación.

### Usa **snake_case** en:

- Nombre de archivos:

      mi_archivo_javascript.js;

### Usa **UPPER_CASE** en:

- Constantes:

```js
const UNA_CONSTANTE = "Soy una constante";
PI = 3.141592653589793;
```

### Usa **UpperCamelCase** en:

- Clases:

```js
class SerHumano {
  constructor(nombre, genero) {
    this.nombre = nombre;
    this.genero = genero;
  }

  miNombreEs() {
    return `Mi nombre es ${this.nombre}`;
  }
}
```

### Usa **lowerCamelCase** en:

- Objetos:

```js
const unObjeto = {
  nombre: "Alexis",
  email: "uriartealexis@gmail.com",
};
```

- Primitivos:

```js
let unaCadena = "Hola Mundo";
unNumero = 19;
unBoolean = true;
```

- Funciones:

```js
function holaMundo(nombre) {
  alert(`Hola mundo ${nombre}`);
}
holaMundo("Alexis");
```

- Instancias:

```js
const ajax = new XMLHttpRequest(),
  ale = new SerHumano("Alexis", "Hombre");
```

## La Consola de JS

Muestra información sobre la página web que se está ejecutando en ese momento, y también incluye la línea de comando que puede usar para ejecutar **_expresiones JS_** en la página actual.

![VerEnGoogle](consola.png)

Muestra la información proporcionada en la consola de Javascript:

```js
console.log("Hola, mundo!");
```

### Concatenación

Une dos valores de tipo _string_ o con alguna _variable_, devolviendo otro string correspondiente a la unión:

```js
console.log("mi" + "string");
```
