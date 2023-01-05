# Webpack/React/Babe

Muchos de nuestros archivos dependerán de otros, por lo que tendremos que importar y exportar componentes. Es por esto que tendremos que instalar todas las dependencias necesarias para nuestro proyecto.

Pasos a seguir:

1. Crearemos un `package.json` con: `npm init` dentro de un directorio vacío.

   **package.json:** Esto guarda las dependencias que hemos instalado y sirve para que cuando compartamos nuestro proyecto con otra persona pueda instalarlas con `npm install`.

2. Instalamos webpack y webpack-cli con: `npm i -D webpack-cli`.

   **webpack:** La base de webpack para crear [bundlers](../../00-Languages/JavaScript/07-MODULES/05-Bundlers.md)
   **webpack-cli:** Sirve para habilitar comandos de webpack en la consola.

3. Instalamos React y ReactDOM con: `npm i react react-dom`.

   **React:** La librería para JvaScript
   **ReactDOM:** Librería de React para trabajar con DOM.

4. Instalamos Babel con todas sus dependencias con: ` npm i -D @babel/core @babel/preset-env @babel/preset-react babel-loader`

   **@babel/core:** es la base de [Babel](https://babeljs.io).
   **@babel/preset-env:** es para que Babel pueda compilar [ECMAScript6](../../00-Languages/JavaScript/05-ES6/ES6.md).
   **@babel/preset-react**: es para que Babel pueda compilar [jsx](./readme.md).
   **babel-loader:** es para que webpack pueda utilizar a Babel.

5. Verificamos nuestro `package.json`:

   ```json
   {
     "name": "instalations",
     "version": "1.0.0",
     "description": "",
     "main": "index.js",
     "scripts": {
       "test": "echo \"Error: no test specified\" && exit 1"
     },
     "author": "",
     "license": "ISC",
     "devDependencies": {
       "@babel/core": "^7.17.5",
       "@babel/preset-env": "^7.16.11",
       "@babel/preset-react": "^7.16.7",
       "babel-loader": "^8.2.3",
       "webpack": "^5.69.1",
       "webpack-cli": "^4.9.2"
     },
     "dependencies": {
       "react": "^17.0.2",
       "react-dom": "^17.0.2"
     }
   }
   ```

6. Creamos un archivo `webpack.config.js` y lo configuramos:

   ```js
   module.exports = {
     entry: "App.js",
     output: {
       path: "./Desktop/Programacion/Henry",
       filename: "bundle.js",
     },
     module: {
       rules: [
         {
           test: /\.(js|jsx)$/,
           exclude: /node_modules/,
           use: {
             loader: "babel-loader",
             options: {
               presets: ["@babel/preset-react", "@babel/preset-env"],
             },
           },
         },
       ],
     },
   };
   ```

   - **ENTRY:** Este será el punto de inicio de webpack. Ponemos el nombre del archivo cabecera.
   - **OUTPUT:** Aquí pondremos el `path/ruta` donde queramos que se guarde nuestro archivo `bundler`. Luego con que nombre se guardará.
   - **MODULE:** En esta parte escribiremos las reglas de configuración.
     Dentro de `test` pondremos el tipo de extensiones que buscamos aplicar la configuración.
     En `exclude` pondremos las carpetas/archivos que queramos excluir de la configuración.
     En `use` pondremos la configuración en sí. Le decimos que utilice _Babel_ para hacer la traducción(compilación).

7. Dentro de `package.json` agregaremos un nuevo script: `build`. Se encargará de ejecutar webpack cuando corramos el comando: `npm build`.

   ```json
   "scripts": {
     "build": "webpack"
   }

    // Puede también estar de esta segunda forma, y dejará un watcher viendo los archivos constantemente.
   "scripts": {
     "build": "webpack -w"
   }
   ```
