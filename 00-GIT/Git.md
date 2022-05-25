# Git

Es un sistema de control de versiones. Quiere decir que registra o guarda cambios de archivos o conjunto de archivos a lo largo del tiempo para poder recuperar versiones anteriores.

## Comenzando a usar Git

### **Comandos básicos**

- `git init`: Se utiliza para iniciar nuestro repositorio.
- `git add ArchivoEjemplo.js`: Crea el archivo pero no lo guarda de forma definitiva, lo almacena en (Staging Area).
- `git commit -m "name_commit"`: Aquí se generan cambios de "Staging Area" y con ( -m "") se deja un mensaje que nos sea útil.
- `git add .`: Agrega los archivos actualizados al repositorio, pero únicamente en la carpeta que te encuentras.
- `git commit -m "Cambios name_commit"`: sirve para generar cambios sobre la versión antigua.
- `git status`: Sirve para revisar si has modificado o guardado los cambios hechos.
- `git log "archivo.txt"`: Sirve para ver el historial del archivo.
- `git push`: Sirve para enviar cambios al repositorio remoto.
- `git pull`: Sirve para recibir cambios de repositorio remoto a local.

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
