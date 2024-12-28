# 📝 Cheatsheet de Comandos 🐧 Termux

### 📦 Comandos Básicos

- **`pkg update`**: Actualiza la lista de paquetes disponibles.
- **`pkg upgrade`**: Actualiza todos los paquetes instalados a sus últimas versiones.
- **`pkg install <paquete>`**: Instala un paquete específico.
- **`pkg uninstall <paquete>`**: Elimina un paquete específico.
- **`pkg list-installed`**: Lista todos los paquetes instalados.
- **`pkg search <paquete>`**: Busca un paquete en los repositorios.

### 🔧 Comandos de Gestión de Usuarios

- **`termux-setup-storage`**: Configura el acceso al almacenamiento del dispositivo.
- **`whoami`**: Muestra el nombre del usuario actual.
- **`passwd`**: Cambia la contraseña del usuario actual.

### 🛠️ Comandos de Gestión de Servicios

- **`termux-wake-lock`**: Mantiene el dispositivo despierto.
- **`termux-wake-unlock`**: Permite que el dispositivo se duerma.

### 📂 Comandos de Gestión de Archivos

- **`ls`**: Lista los archivos y directorios en el directorio actual.
- **`cd <directorio>`**: Cambia al directorio especificado.
- **`pwd`**: Muestra el directorio actual.
- **`cp <origen> <destino>`**: Copia archivos o directorios.
- **`mv <origen> <destino>`**: Mueve o renombra archivos o directorios.
- **`rm <archivo>`**: Elimina un archivo.
- **`rm -r <directorio>`**: Elimina un directorio y su contenido.
- **`mkdir <directorio>`**: Crea un nuevo directorio.
- **`rmdir <directorio>`**: Elimina un directorio vacío.

### 🌐 Comandos de Red

- **`ifconfig`**: Muestra la configuración de red.
- **`ping <host>`**: Envía paquetes ICMP a un host para comprobar la conectividad.
- **`netstat`**: Muestra las conexiones de red, tablas de enrutamiento y estadísticas.
- **`ssh <usuario>@<host>`**: Conecta a un host remoto mediante SSH.
- **`scp <archivo> <usuario>@<host>:<destino>`**: Copia archivos a un host remoto mediante SCP.
- **`wget <URL>`**: Descarga archivos desde la web.
- **`curl <URL>`**: Transfiere datos desde o hacia un servidor.

### 🖥️ Comandos de Sistema

- **`uname -a`**: Muestra información del sistema.
- **`top`**: Muestra los procesos en ejecución y el uso de recursos del sistema.
- **`htop`**: Muestra una vista interactiva de los procesos en ejecución. (Requiere instalación previa con `pkg install htop`)
- **`df -h`**: Muestra el uso del espacio en disco.
- **`du -sh <directorio>`**: Muestra el tamaño de un directorio.
- **`free -h`**: Muestra el uso de la memoria.
- **`uptime`**: Muestra el tiempo que el sistema ha estado en funcionamiento.
- **`dmesg`**: Muestra mensajes del kernel. (Puede no mostrar toda la información sin acceso root)

### 📊 Comandos de Información

- **`ps aux`**: Muestra todos los procesos en ejecución.
- **`who`**: Muestra quién está conectado al sistema.
- **`last`**: Muestra el historial de inicios de sesión.
- **`hostname`**: Muestra o establece el nombre del host.
- **`lscpu`**: Muestra información sobre la CPU.
- **`lsblk`**: Muestra información sobre los dispositivos de bloques.
- **`lspci`**: Muestra información sobre los dispositivos PCI.
- **`lsusb`**: Muestra información sobre los dispositivos USB.

### 🧹 Comandos de Limpieza

- **`pkg clean`**: Limpia los archivos de paquetes descargados.
- **`rm -rf /data/data/com.termux/files/usr/tmp/*`**: Elimina archivos temporales.

### 🛡️ Comandos de Seguridad

- **`termux-fingerprint`**: Utiliza el sensor de huellas dactilares para la autenticación.
- **`termux-tts-speak <texto>`**: Convierte texto a voz.

### 🧩 Comandos de Extensiones

- **`pkg install <paquete>`**: Instala un paquete.
- **`pkg uninstall <paquete>`**: Elimina un paquete.
- **`pkg list-installed`**: Lista los paquetes instalados.

### 📦 Comandos de Paquetes

- **`pkg search <paquete>`**: Busca un paquete en los repositorios.
- **`pkg show <paquete>`**: Muestra información sobre un paquete.
- **`dpkg -i <archivo.deb>`**: Instala un paquete .deb.
- **`dpkg -r <paquete>`**: Elimina un paquete instalado con dpkg.
- **`dpkg -l`**: Lista todos los paquetes instalados con dpkg.

### 🛠️ Comandos de Configuración

- **`nano <archivo>`**: Edita un archivo con el editor Nano.
- **`vim <archivo>`**: Edita un archivo con el editor Vim.

### 📜 Comandos de Registro

- **`logcat`**: Muestra los registros del sistema Android. (Requiere acceso root para funcionar correctamente)
- **`dmesg`**: Muestra mensajes del kernel. (Puede no mostrar toda la información sin acceso root)

### 🗂️ Comandos de Gestión de Distribuciones

- **`termux-info`**: Muestra información sobre la instalación de Termux.
- **`cat /etc/os-release`**: Muestra información sobre la versión del sistema operativo.

### 🧩 Comandos de Integración

- **`pkg install build-essential`**: Instala herramientas esenciales para la compilación de software.
- **`pkg install linux-headers-$(uname -r)`**: Instala los headers del kernel para la versión actual.
- **`pkg install dkms`**: Instala DKMS para la gestión de módulos del kernel.

### 🛠️ Comandos de Diagnóstico

- **`termux-battery-status`**: Muestra el estado de la batería.
- **`termux-wifi-connectioninfo`**: Muestra información sobre la conexión Wi-Fi.
- **`termux-wifi-scaninfo`**: Muestra información sobre las redes Wi-Fi disponibles.
- **`termux-sensor`**: Muestra información sobre los sensores del dispositivo.