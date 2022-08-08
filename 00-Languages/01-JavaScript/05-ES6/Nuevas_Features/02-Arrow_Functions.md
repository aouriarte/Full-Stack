# ARROW FUNCTIONS

Las _Arrow Functions_ son una sintaxis nueva para escribir funciones.

Podemos observar las dos formas de escribir una misma función. La segunda (**arrow function**) no requiere de la palabra clave function:

```js
function normal(x) {
  return x * x;
}

var arrow = (x) => {
  return x * x;
};
```

- Las **arrow functions** tienen la particularidad de que, aunque el argumento **siempre** se puede escribir entre paréntesis, cuando se pasa **un sólo** parámetro no es necesario.

  ```js
  var arrow = (x) => {
    return x * x;
  };
  //El parámetro no tiene paréntesis.

  var arrow = (x) => {
    return x * x;
  };

  var arrow = (x, y) => {
    return x * y;
  };
  ```

- Otra particularidad de esta sintaxis es que, cuando en el cuerpo de la función solo tenemos una línea de código, podemos deshacernos tanto de las llaves como de la palabra clave return.

  ```js
  var nums = [1, 4, 5, 7, 3, 5, 7, 5];
  var cincos = [];

  nums.forEach((x) => {
    if (v % 5 === 0) {
      cincos.push(x);
    }
  });
  ```

- Este ejemplo sirve como demostración de que las arrow functions se pueden usar en cualquier tipo de método también.

  ```js
  var bob = {
    name: "Bob",
    friends: ["Alejo", "Luca", "Manny"],
    printFriends() {
      this.friends.forEach((x) => console.log(this.name + " knows " + x));
    },
  };
  //Bob knows Alejo
  //Bob knows Luca
  //Bob knows Manny
  /*-------------------------------------------------------------*/
  var bob = {
    name: "Bob",
    friends: ["Alejo", "Luca", "Manny"],
    printFriends() {
      this.friends.forEach(function (x) {
        console.log(this.name + " knows " + x);
      });
    },
  };
  //undefined knows Alejo
  //undefined knows Luca
  //undefined knows Manny
  ```

  Por último, en este ejemplo podemos ver que dentro del mismo objeto, aplicamos la misma función, sólo que en una con sitaxis **arrow** y otra **function**.

  Podemos ver que en la que aplicamos sintaxis **function** se imprime `undefined` en lugar de _“Bob”._ Esto es porque en las funciones **arrow** está predefinido el método `.bind()`; y no en **function**.
