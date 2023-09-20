# Estilos

## Legado

Al principio, cuando se creó React, la forma para asociar los estilos a los componentes era distinta a la de ahora.

Veamos que en el siguiente archivo tenemos un componente a partir de la sintaxis de `class`, y también estamos importando un archivo `css`.

```js
// Componente.jsx
import React from "react";
import "./App.css";

class App extends React.Component {
  render() {
    return (
      <div className="App">
        <h1>Título</h1>
      </div>
    );
  }
}
export default App;
```

Estamos asignando este archivo css como atributo del componente.
Destaquemos que, como estamos trabajando con React, la palabra `class` está reservada para crear [Componentes de Clase](./01-Componentes.md). Es por esto que, cuando queremos atribuirle una propiedad a un `<tag>` ya no lo haremos con `class=""`, sino que ahora lo haremos con la palabra reservada `className=""`.

### Webpack Config

El archivo `Componente.jsx` puede importar el archivo `App.css` gracias a Webpack. Para poder lograr esto tendremos que descargar un nuevo _loader_. Veamos los siguientes pasos:

1. En [Intro](./00-Intro.md) vimos como instalar todos los paquetes de Babel, Webpack y React para nuestro proyecto. Volvamos a ese directorio y continuemos desde aquí para instalar los nuevos paquetes de css.

2. Instalaremos la dependencia con: `npm i --save-dev css-loader style-loader`

   **css-loader** & **style-loader:** Nos permitirán importar y exportar archivos css.

3. Una vez instalado los paquetes css tendremos que configurar webpack en el archivo `webpack.config.js`.

   Le agregamos esto:

   ```js
   module: {
     rules: [
       {
         test: /\.css$/,
         use: ["style-loader", "css-loader"],
       },
     ],
   },
   ```

### PROS Y CONTRAS

- **PROS:** Se da estilos igual que antes, se puedem reutilizar los que ya teníamos.
- **CONTRAS:** Los estilos son globales, va encontra de la idea de los componentes.

---

## Inline Styling (css-in-js)

Escribiremos css pero adentro de JavaScript.

```jsx
const estiloDiv = {
	color: 'blue',
	backgroundImage: 'url(' + imgUrl + ')',
};

function ComponenteSaludo() {
  return (
    <div style={divStyle}>Hello World!</div>;
  )
}
```

Por ejemplo, podremos usar objetos con estilos definidos dentro, de modo que si queremos asignarle un estilo a un `<div>` y luego darle estilo a otro se puede. Lo hacemos entre `style={}`.

> Una **característica** muy importante es que, cuando definimos estilos dentro de un objeto, las propiedades que llevan un `-` tendrán una modificación. Por ejemplo background-image ahora será backgroundImage. La modificación es quitarle el `-` y utilizar [camelCase](../../00-Languages/JavaScript/readme.md).

### PROS Y CONTRAS

- **PROS:** No necesitamos ningún loader. No pueden haber colisiones css.
- **CONTRAS:** Perdemos los `pseudoSelectores`(hover, etc).

---

## CSS Modules

Esta idea recoge las características de los dos estilos anteriores. Lo que haremos es escribir módulos de css (archivos individuales) e importarlos en los componentes que queramos.

Usaremos webpack, ya que tendremos que importar los archivos css,

### Webpack Config

1. Instalamos la dependencia con: `npm i --save-dev css-loader style-loader`.

2. Configuramos webpack.

   ```js
       {
         test: /\.css$/,
         use: [{ loader: "style-loader" },
         { loader: "css-loader",
             options: {
                modules: {
                    localIdenName: "[local]__[hash:base64:5]"
                }
             }
         }],
       },
   ```

   Lo que nos permite hacer esta configuración es que cada vez que webpack lea un archivo css, a cada una de las propiedades de dentro les **hasheará** el nombre, de modo tal que ahora esta propiedad será única. Entonces, si nos encontramos en otro archivo css una propiedad que se llama igual, no tendremos problemas al usarla.

   Ejemplo:

   ```css
   // Estilos css
   .first {
     color: green;
     background-color: blue;
   }

   .saludo {
     font-size: 3px;
   }
   ```

   ```jsx
   // Component.jsx
   import React from "react";
   import dat from "./Estilos.css";

   function Component() {
     return (
       <div>
         <div className={`$.{dat.first} $.{dat.saludo}`}>
           <h2 className={dat.saludo}>Los saludo queridos amigos</h2>
         </div>
       </div>
     );
   }
   ```

---

## STYLED COMPONENTS

La idea de los **styled components** es reforzar buenas prácticas quitando el mapeo entre los estilos y los componentes. Es decir, cuando nosotros exportemos componentes, estos ya van a estar estilizados.

Para usarlo tenemos que instalar las dependencias con: `npm i --save-dev styled-components`

La lógica de esto es primero estilizar el componente para luego armarlo y exportarlo.

```jsx
import styled from "styled-components";

const divEstiler = styled.div`
  width: 50%;
  border: 2px solid black;
`;

export default function Component() {
  return (
    <divEstiler>
      <p>Hello World!</p>
    </divEstiler>
  );
}
```

La idea es crear `<tags>` _personalizados_. Se crea una variable que guardará: `styled`, un `.` + el tagDeReferencia. Luego, a la hora de hacer el componente, directamente lo creamos con este nuevo `<tag>` que hemos creado.
