# DOM API

El _browser_ nos da una _API_ para interactuar con el DOM usando JavaScript. Esta _API_ nos permite:

- Inspeccionar los elementos y la estructura del documento.
- Modificar la estructura, agregar o eliminar elementos html o atributos.
- Modificar el contenido del documento.
- Modificar los estilos (CSS).
- Agregar, eliminar o reaccionar eventos.

El estilo que tiene un archivo _html_, por convención, se lo hace en _css_. Sin embargo, desde JavaScript también podemos realizar cambios en el estilo de nuestra página. A esto se lo conoce como **_cambios dinámicos_**, y están precedidos por un _evento_.

## OBJETO _DOCUMENTO_

Mediante la **ejecución de Javascript** tenemos la posibilidad de acceder a un objeto global denominado **_document_** que contiene las propiedades del DOM y métodos de su _prototype_ que nos permiten acceder a los elementos del DOM y manipularlos.

- **SELECTORES:**
  Este objeto **_document_**, tiene sus métodos y propiedades. Algunos de sus métodos se los denomina **_Selectores_**. Estos nos permiten buscar y recuperar un elemento del DOM, sólo que ahora el elemento retornado es un objeto JS que representa una entidad _html_:

  - **Document.getElementById**(String Id):
    retorna un objeto con referencia a la identidad (Id) del elemento:

    ```js
    <!DOCTYPE >
    <html>
      <head>
        ...
      </head>
      <body>
        <h1 id="titulo">Bienvenidos</h1>
        <h2>Soy Alexis</h2>
      </body>
    </html>

    var title = document.getElementById("titulo");
    title //<h1 id="titulo">Bienvenidos</h1>
    ```

  - **Document.getElementByClassName**(divClass):
    retorna un objeto con referencia a la clase del elemento:

    ```js
    <!DOCTYPE>
    <html>
    <head> ... </head>
    <body>
    	<h1 id="titulo">Bienvenidos</h1>
    	<h2>Soy Alejo</h2>
    	<p class="text">Este texto sirve como ejemplificación.Lo importante es la clase</p>
    </body>
    </html>

    var texto = document.getElementsByClassName("text");
    texto //<p class="text">Este texto sirve como ejemplificación.Lo importante es la clase</p>
    ```

  - **Document.getElementsByTagName():**
    este método nos permite acceder a elementos que tengan el mismo etiquetado:

    ```js
    <!DOCTYPE>
    <html>
    	<head> ... </head>
    	<body>
    		<h1 id="titulo">Bienvenidos</h1>
    		<h2>Soy Alejo</h2>
    		<p class="text">Este texto sirve como ejemplificación.Lo importante es la clase</p>
    		<p>Este es otro texto que no tiene importancia, solo la etiqueta</p>
    	</body>
    </html>

    var parrafos = document.getElementsByTagName("p");
    parrafos //<p class="text">Este texto sirve como ejemplificación.Lo importante es la clase</p>
    		 //<p>Este es otro texto que no tiene importancia, solo la etiqueta</p>
    ```

  - **Document.querySelector**(# | . | “”):
    este método nos retornará tan solo el primer elemento que encuentre de lo que pongamos como argumento.
    En el argumento podemos pasar tres valores distintos:

    ```js
    //Para encontrar el primer Id = "titulo" del archivo:
    document.querySelector(#titulo)
    //Para encontrar la primera class = "text" del archivo:
    document.querySelector(.text)
    //Para encontrar el primer elemento con esa etiqueta del archivo:
    document.querySelector("p")
    ```

  - **Document.querySelectorAll():**
    en este caso pasa lo mismo que en el anterior, con la diferencia que el anterior solo retornaba el primer elemento, y este retornará **todos**.

---

## OTROS MÉTODOS _DOCUMENT_

- **document.bgColor:** retorna o establece el color de fondo del documento.

- **document.body:** retorna el elemento _body_.

- **document.linkColor:** retorna o establece el color de los hipervínculos del documento.

- **document.links:** retorna una lista de todos los hipervínculos.

- **document.caretPositionFromPoint(Number x, Number y):** retorna una posición basado en un eje cartesiano.

- **document.createAttribute(\***string name**\*):** crea un nuevo atributo y lo retorna.

- **document.createElement(\***string name**\*):** crea un nuevo elemento con la etiqueta del parámetro.

- **document.createEvent(\***string interface**\*):** crea un nuevo evento.

- **document.getElementsByName(\***string name**\*):** retorna una lista de todos los elementos pasados por parámetro.

---

## MÉTODOS DE _ELEMENT_

- **element.attributes:** retorna todos los atributos asociados al elemento.

- **element.className:** retorna la clase del elemento.

- **element.id:** retorna el Id del elemento.

- **element.innerHTML:** permite editar el contenido del elemento.

- **element.addEventListener():** registra un controlador de evento para uno específico en el elemento.

- **element.appendChild():** inserta un nodo hijo al elemento.

- **element.setAttribute():** establece un nuevo atributo al elemento.

- **element.classList:** nos permite ingresar a la lista de clases del elemento. Existen métodos internos. `add()` añade clases, `remove()` las borra, `contains()` busca la clase definida y `repleace(oldClass, newClass)` nos permite reemplazar la clase.

- **element.style:** permite atributos visuales de un elemento. A su vez tienen más propiedades.
  `.color() .hegith() .background()`
