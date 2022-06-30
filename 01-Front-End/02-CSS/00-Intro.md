- Universal - = \* para todo de tipo - nombre de la etiqueta
- Descendiente - casi igual que tipo pero un mejor uso cuando sea en el mismo parrafou oración.
- pseudo clases - se pinta cuando pasamos el mouse encima

Especifidad:
-Pseudo-clases
-Elementos
-Pseudo elementos

---

## Selectores

Para insertar propiedades:

```css
 /* En línea */
<h2 style="propiedad: valor;"> Título 2 </h2>

/* Selectores */
<style>
  h2 {
    propiedad: valor;
  }
</style>

/* Clases */
<style>
  .creo-miclase {
    propiedad: valor;
  }
</style>

<h2 class="creo-miclase"> Título 2</h2
<img class="class1 class2"> /* anidar clases */

/* ID */
<style>
  #element-color {
    propiedad: valor;
}
</style>

<h2 id="element-color"> </h2> /* Se puede usar solo una vez */

/* Atributos */
/* busca estilos que tengan un valor de atributo específico */
<style>
  [type='radio'] {
    propiedad: valor;
  }
</style>
```

## Propiedades:

```css
<style>
h1 {
  font-size: 30px; /* tamaño de fuente en un elemento */
  font-family: Arial, sans-serif; /* fuente de un elemento (oficial y suplente) */
}

.class-image {
  width: 500px; /* tamaño de imagen */

}

.class-bordes { /* para bordes */
  border-color: red; /* color */
  border-width: 5px; /* tamaño */
  border-style: solid; /* estilo */
  border.radius: 10px; /* esquinas rondeadas */
}

.class-background {
  background-color: silver; /* fondo de un elemento  */
}

</style>
```

```css
/* Hay tres propiedades importantes que controlan el espacio que rodea cada elemento HTML: padding (relleno), border (borde) y margin (margen). */

/*El margin (margen) de un elemento controla la cantidad de espacio entre su border y los elementos que lo rodean.*/

<style>
  .injected-text {
    margin-bottom: -25px;
    text-align: center;
  }

  .box {
    border-style: solid;
    border-color: black;
    border-width: 5px;
    text-align: center;
  }

  .yellow-box {
    background-color: yellow;
    padding: 10px;
  }

  .red-box {
    background-color: crimson;
    color: #fff;
    padding: 20px;
  }

  .blue-box {
    background-color: blue;
    color: #fff;
    padding: 20px;
  }
</style>
<h5 class="injected-text">margin</h5>

<div class="box yellow-box">
  <h5 class="box red-box">padding</h5>
  <h5 class="box blue-box">padding</h5>
</div>

/* CSS te permite controlar por separado el padding de los cuatro lados individuales de un elemento por medio de las propiedades padding-top, padding-right, padding-bottom y padding-left. */

<style>
.blue-box {
    background-color: blue;
    color: #fff;
    padding-top: 40px;
    padding-right: 20px;
    padding-bottom: 20px;
    padding-left: 40px;
  }
</style>

/* En lugar de especificar las propiedades padding-top, padding-right, padding-bottom, y padding-left individualmente, puedes especificarlas todas en una sola línea, como se muestra a continuación: */

<style>
.blue-box {
    background-color: blue;
    color: #fff;
    padding: 10px 20px 10px 20px;
    margin: 20px 40px 20px 40px;
  }
</style>
/* Estos cuatro valores se leen en el sentido de las agujas del reloj: arriba, derecha, abajo, izquierda, (top, right, bottom, left)
Se puede hacer lo mismo con margin (margen) */
```

### Unidades absolutas y relativas de medida

Los `px`  (píxeles) son un tipo de unidad de longitud que le indica al navegador qué tamaño o cuánto espaciado asignarle a un elemento.

- Las unidades absolutas están relacionadas con unidades físicas de longitud. Por ejemplo: `in` y `mm` se refieren a pulgadas y milímetros. Las unidades de longitud absoluta *aproximan la medición real sobre una pantalla*, **pero existen cierta variación que depende de la resolución de la pantalla utilizada**. 

- Las unidades relativas, como `em` o `rem` son relativas a otro valor de longitud.
Por ejemplo `em` es para definir el tamaño de fuente de un elemento.  Si la utilizas para establecer la propiedad font-size, es relativa al font-size del elemento padre.

## Orden de Selectores


En línea
Id
Class
General (body)