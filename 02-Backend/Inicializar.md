# Inicializar repositorios (Back-End)

## Comandos

- `npm init -y` </br>
  Inicializar un proyecto con su `package.json`.

- `npm install "dependencia" -D` </br>
  Instalar como dependencia de desarrollo.

### TypeScript

- `npx tsc --init` </br>
  Crear el `tsconfig.json`.

- `npm i ts-node-dev -D` </br>
  Se usa en vez de nodemon.

- `package.json` </br>
  Configurar:
  ```json
  tsc: tsc (compila Ts a Js)
  start: node build/index.js (crear carpeta build.js)
  dev: ts-node-dev index.ts (para la terminal)
  ```
