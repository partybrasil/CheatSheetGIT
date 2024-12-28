# 📝 Cheatsheet de Comandos

---

## 🐙 GIT

### 📦 Comandos Básicos

- **`git init`**: Inicializa un nuevo repositorio Git.
- **`git clone <url>`**: Clona un repositorio remoto.
- **`git add <archivo>`**: Añade archivos al área de preparación.
- **`git commit -m "mensaje"`**: Realiza un commit con un mensaje.
- **`git status`**: Muestra el estado de los archivos.
- **`git log`**: Muestra el historial de commits.
- **`git diff`**: Muestra las diferencias entre archivos.
- **`git branch`**: Lista las ramas locales.
- **`git checkout <rama>`**: Cambia a una rama específica.
- **`git merge <rama>`**: Fusiona una rama con la actual.
- **`git pull`**: Actualiza el repositorio local desde el remoto.
- **`git push`**: Envía los commits locales al repositorio remoto.
- **`git fetch`**: Descarga objetos y referencias desde otro repositorio.
- **`git remote -v`**: Muestra las URLs de los repositorios remotos.
- **`git reset <archivo>`**: Quita un archivo del área de preparación.
- **`git revert <commit>`**: Crea un nuevo commit que revierte uno anterior.
- **`git stash`**: Guarda temporalmente los cambios no confirmados.
- **`git stash pop`**: Aplica los cambios guardados en el stash.
- **`git tag <nombre>`**: Crea una nueva etiqueta.
- **`git show <objeto>`**: Muestra información sobre un objeto Git.
- **`git rm <archivo>`**: Elimina un archivo del repositorio y del área de preparación.
- **`git mv <archivo>`**: Mueve o renombra un archivo.
- **`git bisect`**: Usa la búsqueda binaria para encontrar el commit que introdujo un bug.
- **`git cherry-pick <commit>`**: Aplica los cambios de un commit específico.
- **`git rebase <rama>`**: Reaplica commits sobre otra base.
- **`git config <clave> <valor>`**: Establece una configuración de Git.
- **`git archive <rama>`**: Crea un archivo tar o zip de los archivos en una rama.
- **`git blame <archivo>`**: Muestra qué commit y autor modificaron cada línea de un archivo.
- **`git clean -f`**: Elimina archivos no rastreados del directorio de trabajo.

---

## 🐙 GitHub-CLI

### 📦 Comandos Básicos

- **`gh auth login`**: Inicia sesión en GitHub.
- **`gh auth logout`**: Cierra sesión en GitHub.
- **`gh auth status`**: Muestra el estado de autenticación.
- **`gh repo create`**: Crea un nuevo repositorio.
- **`gh repo clone <repo>`**: Clona un repositorio de GitHub.
- **`gh repo fork <repo>`**: Crea un fork de un repositorio.
- **`gh repo view <repo>`**: Muestra detalles de un repositorio.
- **`gh issue list`**: Lista las issues de un repositorio.
- **`gh issue create`**: Crea una nueva issue.
- **`gh issue view <issue>`**: Muestra detalles de una issue.
- **`gh pr create`**: Crea un nuevo pull request.
- **`gh pr list`**: Lista los pull requests de un repositorio.
- **`gh pr view <pr>`**: Muestra detalles de un pull request.
- **`gh pr merge <pr>`**: Fusiona un pull request.
- **`gh pr checkout <pr>`**: Cambia a la rama de un pull request.
- **`gh release create <tag>`**: Crea una nueva release.
- **`gh release list`**: Lista las releases de un repositorio.
- **`gh release view <tag>`**: Muestra detalles de una release.
- **`gh release delete <tag>`**: Elimina una release.

---


## 🛠️ Windows Package Manager (WinGet)

### 📦 Comandos Básicos

- **`winget search <paquete>`**: Busca un paquete.
- **`winget install <paquete>`**: Instala un paquete.
- **`winget list`**: Lista los paquetes instalados.
- **`winget upgrade`**: Actualiza todos los paquetes instalados.
- **`winget uninstall <paquete>`**: Desinstala un paquete.
- **`winget source list`**: Lista las fuentes de paquetes.
- **`winget source add <nombre> <url>`**: Añade una nueva fuente de paquetes.
- **`winget show <paquete>`**: Muestra información detallada de un paquete.
- **`winget validate <archivo>`**: Valida un archivo de manifiesto.
- **`winget hash <archivo>`**: Genera el hash SHA256 de un archivo.
- **`winget export -o <archivo>`**: Exporta la lista de paquetes instalados a un archivo.
- **`winget import -i <archivo>`**: Importa y reinstala paquetes desde un archivo.
- **`winget settings`**: Abre el archivo de configuración de winget.
- **`winget features`**: Muestra las características experimentales disponibles.
- **`winget --version`**: Muestra la versión de winget instalada.

---

## 🐧 WSL2

### 📦 Comandos Básicos

- **`wsl --install`**: Instala WSL y la distribución predeterminada.
- **`wsl --list --online`**: Lista las distribuciones disponibles para instalar.
- **`wsl --install -d <distro>`**: Instala una distribución específica.
- **`wsl --set-default <distro>`**: Establece la distribución predeterminada.
- **`wsl --list --verbose`**: Lista las distribuciones instaladas con detalles.
- **`wsl --terminate <distro>`**: Termina una distribución específica.
- **`wsl --shutdown`**: Apaga todas las distribuciones de WSL.
- **`wsl`**: Inicia la distribución predeterminada.
- **`wsl --update`**: Actualiza WSL a la última versión.
- **`wsl --export <distro> <archivo>`**: Exporta una distribución a un archivo tar.
- **`wsl --import <distro> <directorio> <archivo>`**: Importa una distribución desde un archivo tar.
- **`wsl --set-version <distro> <version>`**: Establece la versión de WSL para una distribución específica.
- **`wsl --unregister <distro>`**: Desregistra una distribución, eliminándola completamente.

---

## 🐳 Docker

### 📦 Comandos Básicos

- **`docker --version`**: Muestra la versión de Docker instalada.
- **`docker pull <imagen>`**: Descarga una imagen desde Docker Hub.
- **`docker build -t <nombre>:<tag> <ruta>`**: Construye una imagen desde un Dockerfile.
- **`docker run <imagen>`**: Ejecuta un contenedor basado en una imagen.
- **`docker ps`**: Lista los contenedores en ejecución.
- **`docker ps -a`**: Lista todos los contenedores, incluyendo los detenidos.
- **`docker stop <contenedor>`**: Detiene un contenedor en ejecución.
- **`docker rm <contenedor>`**: Elimina un contenedor detenido.
- **`docker rmi <imagen>`**: Elimina una imagen de Docker.
- **`docker exec -it <contenedor> <comando>`**: Ejecuta un comando en un contenedor en ejecución.
- **`docker-compose up`**: Levanta todos los servicios definidos en un archivo `docker-compose.yml`.
- **`docker-compose down`**: Detiene y elimina todos los contenedores definidos en un archivo `docker-compose.yml`.

---

## 💻 Terminal

### 📦 Comandos Básicos

- **`ls`**: Lista los archivos y directorios en el directorio actual.
- **`cd <directorio>`**: Cambia al directorio especificado.
- **`pwd`**: Muestra la ruta del directorio actual.
- **`mkdir <directorio>`**: Crea un nuevo directorio.
- **`rm <archivo>`**: Elimina un archivo.
- **`rm -r <directorio>`**: Elimina un directorio y su contenido de forma recursiva.
- **`cp <origen> <destino>`**: Copia un archivo o directorio.
- **`mv <origen> <destino>`**: Mueve o renombra un archivo o directorio.
- **`touch <archivo>`**: Crea un nuevo archivo vacío.
- **`cat <archivo>`**: Muestra el contenido de un archivo.
- **`nano <archivo>`**: Abre un archivo en el editor de texto Nano.
- **`vim <archivo>`**: Abre un archivo en el editor de texto Vim.
- **`grep <patrón> <archivo>`**: Busca un patrón en un archivo.
- **`find <directorio> -name <nombre>`**: Busca archivos y directorios por nombre.
- **`chmod <permisos> <archivo>`**: Cambia los permisos de un archivo.
- **`chown <usuario>:<grupo> <archivo>`**: Cambia el propietario y grupo de un archivo.
- **`df -h`**: Muestra el uso del espacio en disco de forma legible.
- **`du -h <directorio>`**: Muestra el uso del espacio en disco de un directorio.
- **`ps aux`**: Muestra información sobre los procesos en ejecución.
- **`kill <pid>`**: Termina un proceso por su ID.
- **`top`**: Muestra los procesos en ejecución en tiempo real.
- **`htop`**: Muestra una vista interactiva de los procesos en ejecución.
- **`tar -czvf <archivo.tar.gz> <directorio>`**: Crea un archivo tar comprimido con gzip.
- **`tar -xzvf <archivo.tar.gz>`**: Extrae un archivo tar comprimido con gzip.
- **`zip -r <archivo.zip> <directorio>`**: Crea un archivo zip de un directorio.
- **`unzip <archivo.zip>`**: Extrae un archivo zip.
- **`ssh <usuario>@<host>`**: Conecta a un host remoto vía SSH.
- **`scp <archivo> <usuario>@<host>:<destino>`**: Copia archivos a un host remoto vía SCP.
- **`curl <url>`**: Realiza una solicitud a una URL.
- **`wget <url>`**: Descarga archivos desde una URL.
- **`history`**: Muestra el historial de comandos ejecutados.
- **`alias <nombre>='<comando>'`**: Crea un alias para un comando.
- **`unalias <nombre>`**: Elimina un alias.

---