# Eventos

[JQuery](https://jquery.com/) es una librería de JavaScript que nos permite manipular el DOM, manejar eventos e implementar AJAX.

```js
$(".answer").click(function () {
  let meal = {
    location: "here",
    condiments: "ketchup",
    idNumber: 191,
  };

  // data contiene los datos del servidor
  $.get("/comboMeal", meal, function (data) {
    eat(data);
  });
});
```

El signo `"$"` es un encabezador que emula un selector, pero para **JQuery**. Entre paréntesis va lo que queremos seleccionar; en este caso la _class answer_. Para definirle un **addEventListenet**, directamente ponemos la acción precedida de un `"."` ; en este caso `.click` . Posteriormente ponemos la función que queramos que se ejecute.

Lo que está sucediendo en la segunda parte del código es que, con `$.get()` , **JQuery** está haciendo una petición del tipo _get_. La petición se la está haciendo a la ruta `'/comboMeal'` (primer parámetro). El segundo parámetro es la información que estamos pidiendo, es decir, `meal`. Por último, una vez que recibimos la información, se ejecutará la función `eat(data)` .
