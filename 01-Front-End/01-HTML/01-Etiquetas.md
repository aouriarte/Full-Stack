# Etiquetas

Algunas etiquetas de html no necesitan tener nada adentro, por lo tanto podemos abreviar su escritura poniendo un "`/`" antes del bracket final.

```html
<img src="https://imagen.com/img.jpg />
```

- `<br>` : Único tag que es solo. Sirve para llenar espacios en blanco o como espacio.
- `<p>` : Indica un párrafo.
- `<center>` : Para centrar.

## Estilos de Letra:

```html
<b> negrita </b>
<i> itálica </i>
<strike> tachada </strike>
<small> chiquita </small>
```

## Listas:

```html
<ul> Desordenadas
  <li></li>
</ul>
<ol> Ordenadas
  <li>Contenido de las listas</li>
</ol>
```

## Vínculos:

```html
<a href="https://www.tuEnlace.com" target="_BLANCK"> Click Aquí </a>
<!-- href="" para insertar un enlace -->
<!-- target="_BLANCK" nos permite abrir el enlace en otra pestaña -->

<!-- También podemos hacer vínculos dentro de nuestra propia página -->
<a href="#contactos-header">Contactos</a>
... <!-- con el símbolo '#' para vincular -->
<h2 id="contactos-header">Contactos</h2>
<!-- y agregadno 'id' a donde queramos que vaya>
```

> "https" indica que la página es segura (s).

## Contenido Multimedia

```html
<!-- Imágenes -->
<img
  src="enlace de imagen.png u otro formato"
  widht="ancho de megapíxeles"
  height="alto"
  alt="nombre del archivo"
  title="aparece sobre la imagen al poner el cursor"
/>

<!-- Videos -->
<video src="enlace del video.mp4 u otro formato" controls="necesario"></video>

<!-- Audio -->
<audio src="enlace del audio" controls="necesario"></audio>
```

## Tablas

```html
<table borde="1px">
  <!-- tabla, si queremos le ponemos 'borde' -->
  <tr>
    <!-- columnas o filas -->
    <td>Aquí van los datos</td>
    <td><b> Ejemplo </b></td>
    <td><b> Nombre </b></td>
  </tr>
</table>
```

## Formulario

```html
<form>
  <input type=" " name=" " placeholder="ingresa por favor" required/>
  <!-- 'input' es introducir -->
  <!-- type="puede ser cualquier dato" (password,email,number,submit,etc) -->
  <!-- 'name' para identificar al input -->
  <!-- 'placehoder' es el texto provisional que va en el input-->
  <!-- 'required' quiere decir obligatotio -->
</form>
```

```html
<form action="URL_donde_se guardan_los_datos">
  <input>
</form>
<!-- Con esto podemos construir formularios web que realmente envíen datos a un servidor usando sólo HTML puro -->
```

```html
<form>
  <label for="masculino"> 
    <input id="masculino" value="masculino" type="radio" name="masculino-femenino"> masculino 
  </label>
</form>
<!-- botones radio -->
<!-- Puedes usarlo para hacer preguntas en las que el usuario solo debe dar una respuesta a partir de múltiples opciones -->

<label for="femenino"> 
  <input id="femenino" value="femenino" type="radio" name="masculino-femenino"> femenino 
</label>
<!-- el atributo 'value' reporta el valor de los input al servidor de datos -->
<!-- Cuando el usuario envía el formulario con la opción masculino seleccionada, los datos del formulario incluirán la línea: masculino-femenino=femenino. Esto proviene de los atributos name y value del input "femenino" -->
```

```html
<label for="Acepto"><input id="Acepto" type="checkbox" name="personality"> Acepto</label>
<!-- casillas de verificación -->
<!-- para preguntas que puedan tener más de una respuesta -->
```

## Metadatos

```html
<!-- Cuando alguien busqué alguna palabra en el navegador, le aparecerá nuestra página -->
<meta name="keywords" content="palabras claves de nuestra página" />

<meta name="description" content="descripción de tu página" />

<meta name="author" content="Alexis Uriarte" />

<meta name="copyright" content="si es que tu página es copiada(derechos)" />

<!-- Nos permite indicar cómo se verá un proyecto web en los dispositivos móviles -->
<meta name="viewport" content="width-device-width,initial-scale = 1" />
> Ver más en "Layout"/DOM/DOM-Avanzado

<!-- Codificación para cambiar carácteres -->
<head>
  <title>Título</title>
  <meta charset="utf-8" />
  <!-- Permite tíldes y más -->
</head>
```

## Icono

Poner icono en la pestaña de nuestra página:

```html
<link rel="icono" formato href="nombre del archivo.ico" />
<!-- Con 'ico' cambiamos los 'px' de la imagen -->
```

```html
<main>palabras claves</main> 
<!--Ayuda a los motores de búsqueda y otros desarrolladores a encontrar el contenido principal de tu página (SEO) -->
```