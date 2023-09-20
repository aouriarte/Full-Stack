# Sintaxis

```html
<!-- Elemento o Caja -->
<etiqueta atributo="valor"></etiqueta>
```

## Elementos Básicos

Definimos elementos (etiquetas o tags) con brackets `<>` y un nombre. Los tags se abren y cierran `</>` .

```html
<tag> ... </tag>
```

## Atributos y Valores

En su mayoría, los atributos trabajan en pares de _¨nombre-valor"_

Algunas características importantes:

- Un `atributo` debe tener siempre un espacio entre el nombre de la `etiqueta` .
- El nombre del `atributo` seguido por el signo `=` .
- Comillas dobles o simples para encerrar el `"valor"` .

```html
<button tamaño="pequeño" color="azul"></button>
```

> En realidad se escribe en inglés.

# Etiquetas

## de cabeza:

```html
<head>
  <!---------------------------------- Título -------------------------------->
  <title>Título</title>

  <!-------------------------------- Metadatos ------------------------------>

  <meta charset="utf-8" />
  <!-- Permite tíldes y más -->

  <meta name="keywords" content="palabras claves de nuestra página" />
  <!-- Cuando alguien busqué alguna palabra en el navegador, le aparecerá nuestra página -->

  <meta name="description" content="descripción de tu página" />

  <meta name="author" content="Alexis Uriarte" />

  <meta name="copyright" content="si es que tu página es copiada(derechos)" />

  <meta name="viewport" content="width-device-width,initial-scale=1" />
  <!-- Nos permite indicar cómo se verá un proyecto web en los dispositivos móviles -->

  <!--------------------------------- Script --------------------------------->
  <script src="javascript.js"></script>
  <!-- Enlaza la parte interactiva para nuestra página -->

  <noscript>El navegador no soporta JavaScript</noscript>
  <!-- Definimos contenido alternativo que se muestra cuando el navegador no admite scripts -->

  <!--------------------------------- Style --------------------------------->
  <style>
    p {
      color: white;
      background-color: blue;
    }
  </style>
  <!-- Estilar en línea -->
</head>
```

## de contenido/contenedor:

```html
<!--------------------------------- Encabezados -------------------------------->
<h1>Encabezado</h1>
<h2>...</h2>
<h3>...</h3>
<h4>...</h4>
<h5>...</h5>
<h6>...</h6>

<!------------------------------------- Div ----------------------------------->
<div><!-- content --></div>

<!------------------------------------- Texto --------------------------------->
<p>párrafo</p>

<span>texto</span>
<!-- para aplicar estilo al texto o agrupar elementos en línea -->

<strong>texto marcado</strong>
<!-- para dar mucho énfasis  -->

<em>texto corrido</em>
<!-- para dar énfasis  -->
```

## Listas:

```html
<ul>
  <li>Listas Desordenadas</li>
</ul>

<ol>
  <li>Listas ordenadas</li>
</ol>
```

## Semánticas:

```html
<header><!-- encabezado de navegación --></header>

<main>palabras claves</main>
<!--Ayuda a los motores de búsqueda y otros desarrolladores a encontrar el contenido principal de tu página (SEO) -->

<nav>Enlaces de navegación</nav>

<article><!-- artículo --></article>

<section>Sección</section>

<aside><!-- sección relacionada a lo principal --></aside>

<footer><!-- pie de página --></footer>
```

## Vacías:

Algunas etiquetas de html no necesitan tener nada adentro, por lo tanto podemos abreviar su escritura poniendo un "`/`" antes del bracket final.

```html
<img src="https://imagen.com/img.jpg" />

<br />
<!-- Sirve para espaciado -->
```

## Multimedia:

```html
<!----------------------------------- Imágenes ---------------------------------->
<img
  src="enlace de imagen.png u otro formato"
  widht="ancho de megapíxeles"
  height="alto"
  alt="nombre del archivo"
  title="aparece sobre la imagen al poner el cursor"
/>

<!---------------------------- Videos ------------------------------------------->
<video src="enlace del video.mp4 u otro formato" controls="necesario"></video>

<!---------------------------------------- Audio -------------------------------->
<audio src="enlace del audio" controls="necesario"></audio>
```

## Vínculos:

```html
<a href="https://www.tuEnlace.com" target="_BLANCK"> Click Aquí </a>
<!-- href="" para insertar un enlace -->
<!-- target="_BLANCK" nos permite abrir el enlace en otra pestaña -->

<!-- También podemos hacer vínculos dentro de nuestra propia página -->
<a href="#contactos-header">Contactos</a>
<!-- con el símbolo '#' para vincular -->
<h2 id="contactos-header">Contactos</h2>
<!-- y agregando 'id' a donde queramos que vaya>
```

> "https" indica que la página es segura (s).

## Tablas:

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

## Formulario:

```html
<form>
  <input type=" " name=" " placeholder="ingresa por favor" required />
  <!-- type="puede ser cualquier dato" (password,email,number,submit,etc) -->
  <!-- 'name' para identificar al input -->
  <!-- 'placehoder' es el texto provisional que va en el input-->
  <!-- 'required' quiere decir obligatotio -->
</form>
```

```html
<!----------------------------- botones radio ---------------------------->
<!-- Puedes usarlo para hacer preguntas en las que el usuario solo debe dar una respuesta a partir de múltiples opciones -->

<form action="URL_donde_se guardan_los_datos">
  <!-- Con esto podemos construir formularios web que realmente envíen datos a un servidor usando sólo HTML puro -->

  <label for="masculino">
    <input
      id="masculino"
      value="masculino"
      type="radio"
      name="masculino-femenino"
    />

    masculino
  </label>

  <label for="femenino">
    <input
      id="femenino"
      value="femenino"
      type="radio"
      name="masculino-femenino"
    />
    <!-- el atributo 'value' reporta el valor de los input al servidor de datos -->
    <!-- Cuando el usuario envía el formulario con la opción masculino seleccionada, los datos del formulario incluirán la línea: masculino-femenino=femenino. Esto proviene de los atributos name y value del input "femenino" -->

    femenino
  </label>
</form>
```

```html
<!-------------------------- casillas de verificación ------------------------->
<!-- para preguntas que puedan tener más de una respuesta -->
<label for="Acepto"
  ><input id="Acepto" type="checkbox" name="personality" /> Acepto</label
>
```

## Icono:

Poner icono en la pestaña de nuestra página:

```html
<link rel="icono" formato href="nombre del archivo.ico" />
<!-- Con 'ico' cambiamos los 'px' de la imagen -->
```

## Estilos de Letra:

```html
<b>negrita</b>
<i>itálica</i>
<strike>tachada</strike>
<small>chiquita</small>
```
