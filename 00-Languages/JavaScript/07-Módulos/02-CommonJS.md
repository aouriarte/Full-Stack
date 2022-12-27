# COMMON JS

Permite importar y exportar variables de archivos a otros archivos.

```js
/*ArchivoNumero1.js*/

var names = [
  "Domingo",
  "Lunes",
  "Martes",
  "Miercoles",
  "Jueves",
  "Viernes",
  "Sabado",
];

exports.name = function name(number) {
  return names[number];
};
exports.number = function number(name) {
  return names.indexOf(name);
};
```

La palabra clave `exports` hace referencia a un objeto nativo de JavaScript. Como a cualquier objeto se le pueden agregar distintas propiedades. En este caso hemos agregado la porpiedad `name` y `number`, las cuales son funciones.

Ahora, para poder utilizar las funciones en otros archivos, tenemos que no sólo **exportalas**, sino también **importarlas** en el archivo en el que las queramos usar:

```js
/*ArchivoNumero2.js*/

var weekDays = require("./ArchivoNumero1.js");

console.log(weekDays.name(4)); // Jueves
console.log(weekDays.number("Martes")); // 2
```

Para poder importar en este archivo las funciones que hemos exportado, crearemos una variable nueva en la que guardaremos la importación con la palabra clave `require`_(path/ruta del archivo)_.
