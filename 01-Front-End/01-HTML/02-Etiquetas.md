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
<ul>
  Desordenadas
</ul>
<ol>
  Ordenadas
</ol>
<li>Contenido de las listas</li>
```

## Vínculos:

```html
<a href="https://www.tuEnlace.com" target="_BLANCK"> Click Aquí </a>
<!-- href="" para insertar un enlace -->
<!-- target="_BLANCK" nos permite abrir el enlace en otra pestaña -->
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
  <input type=" " name=" " required="introducir información, es obligatoria" />
  <!-- 'input' es introducir -->
  <!-- type="puede ser cualquier dato" (password,email,number,submit,etc) -->
  <!-- 'name' para identificar al input -->
</form>
```

## Metadatos

```html
<!-- Cuando alguien busqué alguna palabra en el navegador, le aparecerá nuestra página -->
<meta name="keywords" content="palabras claves de nuestra página" />

<meta name="description" content="descripción de tu página" />

<meta name="author" content="Alexis Uriarte" />

<meta name="copyright" content="si es que tu página es copiada(derechos)" />

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
