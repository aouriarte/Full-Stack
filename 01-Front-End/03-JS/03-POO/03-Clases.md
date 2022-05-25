# Clases

Son funciones especiales.Consideradas una mejora sintática sobre la herencia. Proveen una sintaxis más clara y simple para crear objetos y lidiar con la _herencia_.

## Sintaxis

Necesita 2 componentes:

- **Declaración de Clases:** Para declarar una clase se utiliza la palabra reservada `class` , y un nombre para la clase.

```js
class Rectangle {
  constructor(height, width) {
    this.height = alto;
    this.width = ancho;
  }
}
```

- **Expresión de Clases:** Otra namera de definir una clase. Pueden ser nombradas o anónimas.

  - **Anónima:**

  ```js
  var Polígono = class {
    constructor(alto, ancho) {
      this.alto = alto;
      this.ancho = ancho;
    }
  };
  ```

  - **Nombrada:**

  ```js
  var Cuadrado = class Cuadrado {
    constructor(alto, ancho) {
      this.alto = alto;
      this.ancho = ancho;
    }
  };
  ```
