# Objects

Un *objeto* es una colección de datos. Generalmente pueden albergar variables y funciones, que se denominan **_propiedades_** y **_métodos_** al estar dentro.
Usan un concepto llamdado _pares Clave:Valor_.

## Crear Objetos

Hay 2 formas de hacerlo:

```js
var objeto = new Object();

let nuevoObjeto = {
  // objeto literal
  clave1: valor, // separar cada propiedad con ','
  clave2: valor2, // el último no lleva ','
};

nuevoObjeto; // así llamamos al objeto
```

---

## Propiedades

Agreguemos _propiedades_.

```js
var persona = {
  nombre: "María",
  edad: 28,
  profesión: "Astronauta",
};
```

### Acceder a propiedades

Podemos acceder a las propiedades a través de:

- **Notación de Puntos:**

```js
persona.nombre; //'María'
persona.edad; //28
```

- **Notación de Corchetes:**

```js
persona["nombre"]; //'María'
persona["edad"]; //28
```

### Actualizar propiedades

De la misma manera que acedemos, podemos asignar una nueva propiedad:

```js
persona.profesión = "Doctora";
persona["edad"] = 42;
```

### Crear propiedades

Podemos crear nuevas propiedades:

```js
persona.país = "Perú";
persona["ojos"] = "Marrones";
```

### Eliminar propiedades

Lo hacemos con la palabra clave `delete` :

```js
delete persona.profesión; //'Doctora'
```

---

## Métodos

Podemos establecer una _clave_ para un nombre y el _valor_ , para una **función**.

```js
let persona2 = {
  saludar: function () {
    console.log("Buen día!");
  },
};

persona2.saludar(); // Buen día!
```

---

- Objeto General:

```js
let persona = {
  nombre: "Raúl",
  decirHola: function () {
    alert("Hola" + this.nombre + "!");
  },
}; // Hola Raúl!
```

- En métodos:

```js
const user = {
  username: 'alexis.uriarte'
  password: 'contraseña'
  saludar: function() {
      console.log(this.username + ' dice hola!');
  },
};

user.saludar(); // 'alexis.uriarte dice hola!'
```

> **This** Se refiere al objeto actual en que se está escribiendo el código. Puede usarse para acceder a otras _claves_ en el mismo objeto, muy útil en métodos.
