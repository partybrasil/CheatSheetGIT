# 📝 Cheatsheet de Comandos 🐧 Linux

### 📦 Comandos Básicos

- **`sudo apt update`**: Actualiza la lista de paquetes disponibles.
- **`sudo apt upgrade`**: Actualiza todos los paquetes instalados a sus últimas versiones.
- **`sudo apt install <paquete>`**: Instala un paquete específico.
- **`sudo apt remove <paquete>`**: Elimina un paquete específico.
- **`sudo apt autoremove`**: Elimina los paquetes que ya no son necesarios.
- **`sudo apt clean`**: Limpia los archivos de paquetes descargados.
- **`sudo apt full-upgrade`**: Realiza una actualización completa del sistema.
- **`sudo apt update && sudo apt upgrade && sudo apt dist-upgrade`**: Actualiza la lista de paquetes, actualiza todos los paquetes instalados y realiza una actualización completa del sistema, incluyendo cambios en las dependencias y la instalación de nuevos paquetes necesarios.

### 🔧 Comandos de Gestión de Usuarios

- **`sudo adduser <usuario>`**: Añade un nuevo usuario.
- **`sudo deluser <usuario>`**: Elimina un usuario.
- **`sudo passwd <usuario>`**: Cambia la contraseña de un usuario.
- **`sudo usermod -aG <grupo> <usuario>`**: Añade un usuario a un grupo.
- **`sudo groupadd <grupo>`**: Crea un nuevo grupo.
- **`sudo groupdel <grupo>`**: Elimina un grupo.

### 🛠️ Comandos de Gestión de Servicios

- **`sudo systemctl start <servicio>`**: Inicia un servicio.
- **`sudo systemctl stop <servicio>`**: Detiene un servicio.
- **`sudo systemctl restart <servicio>`**: Reinicia un servicio.
- **`sudo systemctl status <servicio>`**: Muestra el estado de un servicio.
- **`sudo systemctl enable <servicio>`**: Habilita un servicio para que inicie al arrancar el sistema.
- **`sudo systemctl disable <servicio>`**: Deshabilita un servicio para que no inicie al arrancar el sistema.

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
- **`htop`**: Muestra una vista interactiva de los procesos en ejecución.
- **`df -h`**: Muestra el uso del espacio en disco.
- **`du -sh <directorio>`**: Muestra el tamaño de un directorio.
- **`free -h`**: Muestra el uso de la memoria.
- **`uptime`**: Muestra el tiempo que el sistema ha estado en funcionamiento.
- **`dmesg`**: Muestra mensajes del kernel.

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

- **`sudo apt autoremove`**: Elimina los paquetes que ya no son necesarios.
- **`sudo apt clean`**: Limpia los archivos de paquetes descargados.
- **`sudo journalctl --vacuum-time=2weeks`**: Elimina los registros del sistema más antiguos de dos semanas.
- **`sudo rm -rf /var/log/*`**: Elimina todos los archivos de registro (usar con precaución).

### 🛡️ Comandos de Seguridad

- **`sudo ufw enable`**: Habilita el firewall UFW.
- **`sudo ufw disable`**: Deshabilita el firewall UFW.
- **`sudo ufw status`**: Muestra el estado del firewall UFW.
- **`sudo ufw allow <puerto>`**: Permite el tráfico en un puerto específico.
- **`sudo ufw deny <puerto>`**: Deniega el tráfico en un puerto específico.
- **`sudo ufw limit <puerto>`**: Limita el tráfico en un puerto específico para prevenir ataques de fuerza bruta.

### 🧩 Comandos de Extensiones

- **`sudo snap install <paquete>`**: Instala un paquete Snap.
- **`sudo snap remove <paquete>`**: Elimina un paquete Snap.
- **`sudo snap list`**: Lista los paquetes Snap instalados.
- **`sudo flatpak install <paquete>`**: Instala un paquete Flatpak.
- **`sudo flatpak remove <paquete>`**: Elimina un paquete Flatpak.
- **`sudo flatpak list`**: Lista los paquetes Flatpak instalados.

### 📦 Comandos de Paquetes

- **`sudo apt search <paquete>`**: Busca un paquete en los repositorios.
- **`sudo apt show <paquete>`**: Muestra información sobre un paquete.
- **`sudo dpkg -i <archivo.deb>`**: Instala un paquete .deb.
- **`sudo dpkg -r <paquete>`**: Elimina un paquete instalado con dpkg.
- **`sudo dpkg -l`**: Lista todos los paquetes instalados con dpkg.

### 🛠️ Comandos de Configuración

- **`sudo nano /etc/hostname`**: Edita el archivo de configuración del nombre del host.
- **`sudo nano /etc/hosts`**: Edita el archivo de configuración de hosts.
- **`sudo nano /etc/fstab`**: Edita el archivo de configuración de sistemas de archivos.
- **`sudo nano /etc/network/interfaces`**: Edita el archivo de configuración de interfaces de red.
- **`sudo nano /etc/resolv.conf`**: Edita el archivo de configuración de resolv.conf.

### 📜 Comandos de Registro

- **`sudo journalctl`**: Muestra los registros del sistema.
- **`sudo journalctl -xe`**: Muestra los registros del sistema con detalles adicionales.
- **`sudo tail -f /var/log/syslog`**: Muestra los últimos registros del sistema en tiempo real.
- **`sudo tail -f /var/log/auth.log`**: Muestra los últimos registros de autenticación en tiempo real.

### 🗂️ Comandos de Gestión de Distribuciones

- **`lsb_release -a`**: Muestra información sobre la distribución de Linux.
- **`cat /etc/os-release`**: Muestra información sobre la versión del sistema operativo.
- **`sudo do-release-upgrade`**: Actualiza a la última versión de la distribución.

### 🧩 Comandos de Integración

- **`sudo apt install build-essential`**: Instala herramientas esenciales para la compilación de software.
- **`sudo apt install linux-headers-$(uname -r)`**: Instala los headers del kernel para la versión actual.
- **`sudo apt install dkms`**: Instala DKMS para la gestión de módulos del kernel.

### 🛠️ Comandos de Diagnóstico

- **`sudo systemctl --failed`**: Muestra los servicios que han fallado.
- **`sudo dmesg | grep -i error`**: Muestra los mensajes del kernel que contienen errores.
- **`sudo journalctl -p 3 -xb`**: Muestra los registros del sistema con prioridad de error.
- **`sudo smartctl -a /dev/sda`**: Muestra el estado SMART de un disco duro.
- **`sudo memtest86+`**: Ejecuta una prueba de memoria.