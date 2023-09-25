# Eventos

Un evento es una señal de que algo sucedió. Todos los nodos del DOM pueden generar estas señales.

El **_Event Listener_** es el encargado de escuchar esas señales.

## ALGUNAS PROPIEDADES:

- **event.altKey:** retorna un valor indicando si la tecla `<alt>` fue pulsada durante el evento.

- **event.ctrlKey:** retorna si la tecla `<ctrl>` fue pulsada durante el evento.

- **event.currentTarget:** retorna una referencia la objeto actual registrado para el evento.

```js
<!DOCTYPE>
<html>
	<head>
		<style>
		.first {
			background-color: darkgreen;
			height: 200px;
		}
		</style>
	</head>
    <body>
        <div class="first">FIRST DAY</div>
        <div class="second">SECOND DAY</div>

        <script>
	        var firstDiv = document.querySelector(".    first");
	        firstDiv.addEventListener("click", function() {
	    	alert("hiciste click");
	        })
        </script>
    </body>
</html>

//ESTO HARÁ QUE CUANDO HAGAMOS CLICK EN ESA PRIMERA DIV APARECERÁ UNA ALERTA.
```

```js
<!DOCTYPE>
<html>
    <head>
	    <style>
	    .first {
	    	background-color: darkgreen;
	    	height: 200px;
	    }
	    .align {
	        display: flex;
	        align.items: center;
	        font-size: large;
	        font-weight: bold;
	    }
	    </style>
    </head>
    <body>
        <div class="first">FIRST DAY</div>
        <div class="first">SECOND DAY</div>
        <div class="first">THIRD DAY</div>

        <script>
	    var allDivs = document.querySelectorAll("div");
	    for(let i = 0; i < allDivs.length; i++){
		  allDivs.addEventListener("click", function(e){
			  e.target.classList.add("align")}
			)
        }
        </script>
    </body>
</html>

/*EN ESTE CASO, EL PARÁMETRO "e" ES EL EVENTO EN SÍ
MISMO*/
```
