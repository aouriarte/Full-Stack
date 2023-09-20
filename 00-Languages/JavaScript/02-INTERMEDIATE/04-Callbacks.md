## Callbacks

Es una función que tiene la capacidad de pasar una función como _argumento_ de una función externa, para completar algún tipo de rutina o acción. Lo usamos como `cb` .

```js
function saludoDeMañana(name) {
  return "Buen día " + name + "!";
}

function saludoDeNoche(name) {
  return "Buenas noches " + name + "!";
}

function saludar(name, cb) {
  return cb(name);
}

saludar("Alexis", saludoDeMañana); // 'Buen día Alexis!'
saludar("Alexis", saludoDeNoche); // 'Buenas noches Alexis!'
```
