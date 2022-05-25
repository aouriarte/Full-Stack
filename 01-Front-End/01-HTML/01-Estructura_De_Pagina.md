# Crear Página

Siempre se debe llevar esta estructura y la etiqueta de "DOCTYPE".

```html
<!DOCTYPE html>
<!-- Significa que es un doc.html última versión -->
<html>
  <!-- Va a contener a todos los demás tags dentro suyo -->
  <head>
    <!-- Contiene información sobre el documento que no queremos ver -->
    <title>Título de nuestra página</title>
    <!-- Se mostrará en la pestaña del navegador -->
  </head>
  <body>
    <!-- Encierra todo lo que queremos ver en la pantalla o página -->
  </body>
</html>
```

> El `<head>` comunmente contiene el título de la página y links a recursos externos que pueda usar la página (javascript o css).

## Estructura

Lo que vemos dentro de la página (body). Nivel semántico.

```html
<body>
  <header>
    <!-- Encabezado -->
    <nav>
      <!-- Barra de navegación -->
      <ul>
        <!-- Aquí irán las partes de nuestra página -->
        <li><a href="index.html"></a>Inicio</li>
        <li><a href="micuenta.html"></a>Mi cuenta</li>
        <li><a href="sobrenosotros.html"></a>Sobre nosotros</li>
      </ul>
    </nav>
  </header>
  <article>
    <!-- Puede haber varios artículos -->
    <section>
      <!-- Pueden haber varias secciones -->
      <h1>Título</h1>
      <h2>Subtítulo</h2>
      <p>parráfo: abcdfasfhaisfhhifhagehadasjhphoeovbxtsig.</p>
    </section>
  </article>
  <aside>
    <!-- Barra extra -->
    <h1>Extra</h1>
    <p>otro párrafo</p>
  </aside>
  <footer>
    <!-- Pie de página (información de contacto y más) -->
    <h4>Copyright. Todos los derechos reservados</h4>
  </footer>
</body>
```
