# Event Loop

`setTimeout()` es una función integrada en Javascript que nos permitirá retrasar el proceso de una función. Existe un espacio llamado _*“Web Apis”*_ en el que es enviado el proceso de esta función. De esta forma JavaScript puede seguir procesando el código sin perder el tiempo en esa función.

Hay que destacar que, una vez enviado el **setTimeout** al **Web Apis**, JavaScript procesará el resto del código, y sólo recibirá el proceso terminado del Web Apis una vez terminada la lectura del código.

Una vez que el **setTimeout** se terminó de procesar en el Web Apis, pasará al **Callback Queue**. Aquí serán enviados todos los procesos que JavaScript deriva, y como dijimos, una vez que el intérprete termina de leer el código, recién ahí serán reintegrados al **Call Stack**.

```js
function saludarMasTarde() {
  var saludo = "Hola";
  setTimeout(function () {
    console.log(saludo);
  }, 3000);
}
saludarMasTarde();
```

En este ejemplo, el proceso es el siguiente. Primero se ejecuta la función saludarMasTarde, y luego, cuando se ejecuta el setTimeout, se lo envía al Web Apis. Cuando termina de procesarse y de transcurrirse el tiempo, se lo envía a el Callback Queue. Durante todo este tiempo, JavaScript sigue ejecutando el código hasta terminarlo. Una vez terminado, recibe la función del Callback Queue.

- **Callback Queue:** Respeta el FIFO (First In First Out)
- **Call Stack:** Y este el LIFO (Last In First Out)
