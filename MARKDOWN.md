# Markdown

Es un lenguaje de marcado que _facilita la aplicación_ de formato a un texto empleando una **serie de caracteres** de una forma especial.

Ejemplos:

---

# Encabezados 1

## Encabezado 2

### Encabezado 3

#### Encabezado 4

##### Encabezado 5

###### Encabezado 6

---

## Citas

> Esto es una cita. -Anónimo
>
> > Puedes anidar citas.

---

## Listas

Sin enumerar: (Añade 4 espacios para anidar listas)

- Elemento 1
  - Elemento 2
    - Elemento 3

Enumerada: (Se puede combinar con las sin enumerar)

1. Elemento 1
2. Elemento 2
3. Elemento 3

---

## Códigos de bloque

```
Creando códigos de bloque.
Puedes añadir tantas líneas y párrafos como quieras.
```

---

## Reglas horizontales

Se utilizan para separar secciones de una manera visual:

---

---

---

## Elemento de Línea

### Enfásis(negritas y cursivas)

_cursiva_ o _cursiva_
**negrita** o **negrita**

O para combinarlas:
**_cursiva y negrita_** o
**_cursiva y negrita_**

---

## Links o Enlaces

### En línea:

[palabra de enlace](http://www.URL.com)

### Como referencia:

[palabra de enlace][nombre de tu referencia]
[nombre de tu referencia]: http://www.URL.com

Ejemplo:

> Me llamo Javier Cristóbal y tengo un blog sobre [productividad mac][blog].
> En dicha [web][blog] recopilo artículos sobre todo lo relacionado con automatización, gestión y eficiencia.
> [blog]: http://limni.net/blog/

### Links automáticos:

Cuando se quiere presentar el enlace completo.
<http://www.tuenlace>

---

## Código

### Código puro:

Con code dentro de <>  
`Esto es una línea de código`

### Texto preformateado: <pre>

(también puedes hacerlo con 4 espacios)

---

## Imágenes

Casi lo mismo como un link, pero se pone ! al principio:
![Texto alternativo](/ruta/a/la/imagen.jpg)

También podrás añadir un título alternativo que es el que se muestra al dejar el cursor del ratón sobre la imagen:

![Texto alternativo](/ruta/a/la/imagen.jpg "Título alternativo")

# Omitir Markdown

Se hace con \ barra invertida antes de cada símbolos:

- Elemento

\ + Elemento
