# 📝 Cheatsheet de Comandos 🐳 Docker

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

### 🔍 Comandos de Inspección

- **`docker inspect <recurso>`**: Muestra información detallada sobre un contenedor o imagen.
- **`docker logs <contenedor>`**: Muestra los logs de un contenedor.
- **`docker events`**: Muestra eventos en tiempo real del servidor Docker.
- **`docker stats`**: Muestra estadísticas de uso de recursos de los contenedores en ejecución.
- **`docker top <contenedor>`**: Muestra los procesos corriendo dentro de un contenedor.

### 🛠️ Comandos de Gestión

- **`docker start <contenedor>`**: Inicia un contenedor detenido.
- **`docker restart <contenedor>`**: Reinicia un contenedor.
- **`docker pause <contenedor>`**: Pausa todos los procesos en un contenedor.
- **`docker unpause <contenedor>`**: Reanuda todos los procesos en un contenedor pausado.
- **`docker rename <contenedor> <nuevo_nombre>`**: Renombra un contenedor.
- **`docker update <contenedor>`**: Actualiza la configuración de un contenedor.
- **`docker kill <contenedor>`**: Envía una señal para detener un contenedor.
- **`docker wait <contenedor>`**: Bloquea hasta que un contenedor se detenga y luego imprime su código de salida.
- **`docker attach <contenedor>`**: Adjunta la entrada, salida y error estándar a un contenedor en ejecución.
- **`docker commit <contenedor> <nuevo_imagen>`**: Crea una nueva imagen desde los cambios en un contenedor.

### 📂 Comandos de Volúmenes

- **`docker volume create <nombre>`**: Crea un nuevo volumen.
- **`docker volume ls`**: Lista todos los volúmenes.
- **`docker volume inspect <volumen>`**: Muestra información detallada sobre un volumen.
- **`docker volume rm <volumen>`**: Elimina un volumen.
- **`docker volume prune`**: Elimina todos los volúmenes no utilizados.

### 🖼️ Comandos de Imágenes

- **`docker images`**: Lista todas las imágenes locales.
- **`docker tag <imagen> <nuevo_nombre>`**: Etiqueta una imagen con un nuevo nombre.
- **`docker push <imagen>`**: Sube una imagen a un repositorio.
- **`docker save -o <archivo.tar> <imagen>`**: Guarda una imagen en un archivo tar.
- **`docker load -i <archivo.tar>`**: Carga una imagen desde un archivo tar.
- **`docker history <imagen>`**: Muestra el historial de capas de una imagen.
- **`docker import <archivo.tar> <nuevo_imagen>`**: Importa el contenido de un archivo tar para crear una nueva imagen.

### 🏗️ Comandos de Redes

- **`docker network create <nombre>`**: Crea una nueva red.
- **`docker network ls`**: Lista todas las redes.
- **`docker network inspect <red>`**: Muestra información detallada sobre una red.
- **`docker network connect <red> <contenedor>`**: Conecta un contenedor a una red.
- **`docker network disconnect <red> <contenedor>`**: Desconecta un contenedor de una red.
- **`docker network rm <red>`**: Elimina una red.
- **`docker network prune`**: Elimina todas las redes no utilizadas.