# 📝 Cheatsheet de Comandos 🐧 WSL2

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

### 🔧 Comandos Avanzados

- **`wsl --mount <device>`**: Monta un disco físico dentro de WSL 2.
- **`wsl --unmount <device>`**: Desmonta un disco físico de WSL 2.
- **`wsl --status`**: Muestra el estado actual de WSL, incluyendo la versión predeterminada y la configuración.
- **`wsl --set-default-version <version>`**: Establece la versión predeterminada de WSL (1 o 2).
- **`wsl --help`**: Muestra la ayuda y los comandos disponibles para WSL.
- **`wsl --exec <command>`**: Ejecuta un comando específico en la distribución predeterminada.
- **`wsl --cd <directory>`**: Cambia el directorio de trabajo predeterminado para WSL.
- **`wsl --user <username>`**: Inicia WSL con un usuario específico.
- **`wsl --import-in-place <distro> <directorio>`**: Importa una distribución en su lugar desde un directorio existente.
- **`wsl --export-in-place <distro> <directorio>`**: Exporta una distribución en su lugar a un directorio existente.

### 🛠️ Comandos de Diagnóstico

- **`wsl --check`**: Verifica si hay actualizaciones disponibles para WSL.
- **`wsl --version`**: Muestra la versión actual de WSL instalada.
- **`wsl --set-default-user <distro> <user>`**: Establece el usuario predeterminado para una distribución específica.
- **`wsl --status`**: Muestra el estado actual de WSL, incluyendo la versión predeterminada y la configuración.
- **`wsl --list --verbose`**: Lista las distribuciones instaladas con detalles.

### 📂 Comandos de Gestión de Archivos

- **`wsl --import-in-place <distro> <directorio>`**: Importa una distribución en su lugar desde un directorio existente.
- **`wsl --export-in-place <distro> <directorio>`**: Exporta una distribución en su lugar a un directorio existente.
- **`wsl --mount <device>`**: Monta un disco físico dentro de WSL 2.
- **`wsl --unmount <device>`**: Desmonta un disco físico de WSL 2.

### 🌐 Comandos de Red

- **`wsl --network <command>`**: Ejecuta comandos relacionados con la configuración de red en WSL.
- **`wsl --status`**: Muestra el estado actual de WSL, incluyendo la versión predeterminada y la configuración.
- **`wsl --shutdown`**: Apaga todas las distribuciones de WSL.

### 🧩 Comandos de Integración

- **`wsl --install --no-launch`**: Instala WSL sin iniciar la distribución predeterminada.
- **`wsl --install --web-download`**: Instala WSL descargando los archivos necesarios desde la web.
- **`wsl --exec <command>`**: Ejecuta un comando específico en la distribución predeterminada.
- **`wsl --cd <directory>`**: Cambia el directorio de trabajo predeterminado para WSL.

### 📜 Comandos de Registro

- **`wsl --register <distro>`**: Registra una nueva distribución en WSL.
- **`wsl --unregister <distro>`**: Desregistra una distribución, eliminándola completamente.
- **`wsl --list --online`**: Lista las distribuciones disponibles para instalar.
- **`wsl --list --all`**: Lista todas las distribuciones, incluyendo las que están en estado de apagado o terminadas.

### 🗂️ Comandos de Gestión de Distribuciones

- **`wsl --list`**: Lista todas las distribuciones instaladas.
- **`wsl --list --quiet`**: Lista las distribuciones instaladas sin detalles adicionales.
- **`wsl --list --all`**: Lista todas las distribuciones, incluyendo las que están en estado de apagado o terminadas.
- **`wsl --set-default <distro>`**: Establece la distribución predeterminada.

### 🖥️ Comandos de Sistema

- **`wsl --set-default-user <user>`**: Establece el usuario predeterminado para la distribución predeterminada.
- **`wsl --set-default-version <version>`**: Establece la versión predeterminada de WSL (1 o 2).
- **`wsl --shutdown`**: Apaga todas las distribuciones de WSL.
- **`wsl --terminate <distro>`**: Termina una distribución específica.

### 📊 Comandos de Información

- **`wsl --info`**: Muestra información detallada sobre la configuración y el estado de WSL.
- **`wsl --status`**: Muestra el estado actual de WSL, incluyendo la versión predeterminada y la configuración.
- **`wsl --list --verbose`**: Lista las distribuciones instaladas con detalles.
- **`wsl --version`**: Muestra la versión actual de WSL instalada.

### 🧹 Comandos de Limpieza

- **`wsl --cleanup`**: Limpia los archivos temporales y las configuraciones obsoletas de WSL.
- **`wsl --unregister <distro>`**: Desregistra una distribución, eliminándola completamente.
- **`wsl --shutdown`**: Apaga todas las distribuciones de WSL.
- **`wsl --terminate <distro>`**: Termina una distribución específica.

### 🛡️ Comandos de Seguridad

- **`wsl --security`**: Muestra y configura las opciones de seguridad para WSL.
- **`wsl --update`**: Actualiza WSL a la última versión.
- **`wsl --check`**: Verifica si hay actualizaciones disponibles para WSL.
- **`wsl --status`**: Muestra el estado actual de WSL, incluyendo la versión predeterminada y la configuración.

### 🧩 Comandos de Extensiones

- **`wsl --extension <command>`**: Ejecuta comandos relacionados con las extensiones de WSL.
- **`wsl --install --no-launch`**: Instala WSL sin iniciar la distribución predeterminada.
- **`wsl --install --web-download`**: Instala WSL descargando los archivos necesarios desde la web.
- **`wsl --exec <command>`**: Ejecuta un comando específico en la distribución predeterminada.

### 📦 Comandos de Paquetes

- **`wsl --package <command>`**: Ejecuta comandos relacionados con la gestión de paquetes en WSL.
- **`wsl --list --online`**: Lista las distribuciones disponibles para instalar.
- **`wsl --list --all`**: Lista todas las distribuciones, incluyendo las que están en estado de apagado o terminadas.
- **`wsl --list --verbose`**: Lista las distribuciones instaladas con detalles.

### 🛠️ Comandos de Configuración

- **`wsl --config <command>`**: Ejecuta comandos relacionados con la configuración de WSL.
- **`wsl --set-default-version <version>`**: Establece la versión predeterminada de WSL (1 o 2).
- **`wsl --set-default <distro>`**: Establece la distribución predeterminada.
- **`wsl --set-default-user <user>`**: Establece el usuario predeterminado para la distribución predeterminada.
- **`wsl --shutdown`**: Apaga todas las distribuciones de WSL.
- **`wsl --terminate <distro>`**: Termina una distribución específica.
