# Git

Es un sistema de control de versiones. Quiere decir que registra o guarda cambios de archivos o conjunto de archivos a lo largo del tiempo para poder recuperar versiones anteriores.

## Comenzando a usar Git

### **Comandos básicos**

1. `git config [options]` <br/> 
- Establece el nombre de usuario y la dirección de correo electrónico para los **commits**:
  ```bash
  git config --global user.name "Auriarte20"
  git config --global user.email      "uriarte2001alexis@gmail.com"
  ```

2. `git init` <br/>
- Inicializa el repositorio como repositorio git:
  ```bash
  git init
  ```

3. `git clone [url]` <br/> 
- Clonamos nuestro repositorio de GitHub o GitLab:
  ```bash
  git clone http://github.com/mirepo/Auriarte20.git
  ```

4. `git status` <br/>
- Sirve para revisar si has modificado o guardado los cambios hechos:
  ```bash
  git status
  ```

5. `git add [Filename(s)]` <br/>
- Crea el archivo pero no lo guarda de forma definitiva, lo almacena en Staging Area:
  ```bash
  git add index.html style.css script.js
  git add . #guarda todos los cambios locales
  ```

6. `git commit -m [mensaje]` <br/>
- Registra los cambios en el repositorio de git guardando un mensaje de registro junto con una ID de compromiso:
  ```bash
  git commit -m "Fix bug"
  git commit -a  #confirma todo el archivo sin mensaje
  ```

7. `git push [Options] [Variable] [Branch]` <br/> 
- Sirve para enviar cambios al repositorio remoto:
  ```bash
  git push
  git push -u origin main
  ```

8. `git pull [Variable] [Branch] o [url]` <br/> 
- Sirve para recibir cambios del repositorio remoto a local:
  ```bash
  git pull origin main
  git push https://github.com/user/repo
  ```

9. `git log`: <br/>
- Muestra el registro de **commits** realizadas hasta ahora en la rama actual:
  ```bash
  git log
  ```

10. `git checkout [Branch]` <br/>
- Pasar de una rama a otra rama:
  ```bash
  git checkout rama1
  git checkout -b rama2 #crea una rama y nos movemod a ella
  ```

11. `git branch [Options] [Branch]` <br/>
- Realiza operaciones sobre la rama especificada:
  ```bash
  git branch #ver ramas
  git branch rama3 #crea una rama
  git branch -m rama4 #renombramos la rama actual
  git branch -d rama2 #eliminamos esa rama
  ```

12. `git merge [Branch]` <br/>

13. `git show [Commit ID]` <br/>

### **Estados de los archivos en Git**

Cuando trabajamos con Git nuestros archivos pueden vivir y moverse entre 4 diferentes estados:

- **Archivos** **_Untracked_**: Archivos sin rastrear, que aún NO viven dentro de Git.

- **Archivos** **_Unstaged_**: Son archivos que viven dentro de Git pero no han sido afectados por el comando `git add` ni mucho menos por `git commit`. Git tiene un registro de estos archivos, pero esta desactualizado.

- **Archivos** **_Staged_**: Viven dentro de Git y hay registro de ellos por que han sido afectados por el comando `git add`, pero aún no han sido guardados definitivamente en el repositorio por que falta ejecutar el comando `git commit`.

- **Archivos** **_Tracked_**: son los archivos que viven dentro de Git. Es rastreado por `git commit` y se envía con `git push` al repo en Github.

### **Comandos para mover archivos entre los estados de Git**

- `git status`: Vemos el estado de todos nuestros archivos y carpetas.

- `git add`: Agregamos archivos al repo propio. Usamos `git add name_archive` o `git add -a` para agregar todos los archivos. También `git add .`

- `git reset HEAD`: Nos ayuda a devolver los archivos del estado _Staged_ a su estado anterior, puede ser a _unstaged_ o _untracked_.

- `git commit`: Confirmamos el cambio de nuestro archivo y Git nos pedira que dejemos un mensaje para recordar los cambios que hicimos: `git commit -m "mensaje"`.

- `git rm`: Este comando necesita algunos de los argumentos para poder ejecutarse correctamente:

  - `git rm --cached`: Mueve los archivos que le indiquemos al estado _Untracked_.
  - `git rm --force`: Elimina los archivos de Git y del disco duro. Git guarda el registro de la existencia de los archivos, por lo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados).
