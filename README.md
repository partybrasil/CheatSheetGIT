# 📝 **Git y GitHub Cheatsheet: Flujo Completo de Desarrollo**

---

## 🚀 **Configuración Inicial del Repositorio**

```bash
# 1️⃣ Inicializar un repositorio local
git init

# 2️⃣ Configurar identidad global (si no está configurado)
git config --global user.name "TuNombre"
git config --global user.email "TuCorreo@example.com"

# 3️⃣ Crear un archivo README.md o cualquier archivo inicial
echo "# MiProyecto" > README.md

# 4️⃣ Agregar todos los archivos al área de preparación (staging)
git add .

# 5️⃣ Realizar el primer commit
git commit -m "Primer commit: inicialización del proyecto"

# 6️⃣ Crear un repositorio remoto en GitHub
# Desde GitHub, crea un nuevo repositorio y copia la URL.

# 7️⃣ Vincular el repositorio local con el remoto
git remote add origin https://github.com/Usuario/MiProyecto.git

# 8️⃣ Subir los cambios iniciales al repositorio remoto
git branch -M main    # Renombrar la rama a 'main', si no existe
git push -u origin main
```

---

## 📂 **Flujo de Trabajo Básico: Añadir, Confirmar y Subir Cambios**

```bash
# 1️⃣ Verificar estado del repositorio
git status

# 2️⃣ Agregar cambios al área de preparación
git add <archivo>          # Para un archivo específico
git add .                  # Para todos los archivos

# 3️⃣ Confirmar cambios con un mensaje
git commit -m "Descripción breve del cambio"

# 4️⃣ Subir los cambios al repositorio remoto
git push origin <rama>
```

---

## 🌿 **Gestión de Ramas (Branches)**

```bash
# 1️⃣ Crear una nueva rama
git branch <nombre-rama>

# 2️⃣ Cambiar a la nueva rama
git checkout <nombre-rama>

# 3️⃣ Crear y cambiar a una nueva rama en un solo paso
git checkout -b <nombre-rama>

# 4️⃣ Listar todas las ramas
git branch

# 5️⃣ Eliminar una rama local
git branch -d <nombre-rama>
```

---

## 🔄 **Fusionar Ramas (Merging)**

```bash
# 1️⃣ Cambiar a la rama destino (por ejemplo, main)
git checkout main

# 2️⃣ Fusionar la rama específica con la actual
git merge <nombre-rama>

# 3️⃣ Resolver conflictos (si ocurren)
# Editar archivos con conflictos, luego:
git add <archivo-con-resolucion>
git commit -m "Conflictos resueltos"
```

---

## ⬇️ **Actualizar el Repositorio Local (Pull)**

```bash
# Obtener y fusionar cambios del repositorio remoto
git pull origin <rama>
```

---

## 🔍 **Gestión de Historial y Restauración de Cambios**

```bash
# 1️⃣ Mostrar el historial de commits
git log                    # Ver historial completo
git log --oneline          # Ver historial resumido

# 2️⃣ Ver diferencias entre commits
git diff                   # Ver cambios no confirmados
git diff <commit1> <commit2>

# 3️⃣ Deshacer cambios
git restore <archivo>       # Restaurar un archivo al último commit
git restore --staged <archivo>  # Quitar un archivo del área de preparación

# 4️⃣ Resetear commits (con cuidado)
git reset --soft HEAD~1     # Mantener cambios en el área de preparación
git reset --mixed HEAD~1    # Mantener cambios en el directorio de trabajo
git reset --hard HEAD~1     # Deshacer todos los cambios y commits
```

---

## 🛠️ **Escenarios de Recuperación y Reparación de Commits**

```bash
# 1️⃣ Recuperar un commit eliminado
git reflog                  # Ver historial de referencias
git checkout <hash-commit>

# 2️⃣ Crear un commit nuevo corrigiendo el anterior
git commit --amend -m "Nuevo mensaje para el último commit"

# 3️⃣ Volver a un commit anterior sin borrar commits posteriores
git checkout <hash-commit>
```

---

## 🔗 **Pull Requests (PR) en GitHub**

1️⃣ **Crear un Pull Request:**
    - Desde la pestaña **Pull Requests** en GitHub, selecciona la rama que deseas fusionar con `main`.

2️⃣ **Revisión de Código:**
    - Asigna revisores para verificar los cambios.

3️⃣ **Fusionar el PR:**
    - Una vez aprobado, usa el botón **Merge Pull Request** en GitHub.

---

## 📌 **Flujo Completo de Desarrollo Diario**

```bash
# 1️⃣ Actualizar la rama local antes de trabajar
git pull origin main

# 2️⃣ Crear una rama nueva para tu tarea
git checkout -b feature/nueva-funcionalidad

# 3️⃣ Hacer cambios y confirmar
git add .
git commit -m "Implementar nueva funcionalidad"

# 4️⃣ Subir la rama al repositorio remoto
git push origin feature/nueva-funcionalidad

# 5️⃣ Crear un Pull Request desde GitHub

# 6️⃣ Resolver conflictos (si los hay)
git merge origin/main
```

---

## 💡 **Atajos y Trucos Útiles**

- **Stash:** Guarda cambios temporalmente sin confirmar.  
  ```bash
  git stash          # Guardar cambios
  git stash apply    # Recuperar cambios
  ```

- **Alias para comandos comunes:**  
  ```bash
  git config --global alias.co checkout
  git config --global alias.br branch
  git config --global alias.ci commit
  ```

---

## 🖥️ **Uso de GitHub CLI (gh)**

---

### 🚀 **Instalación de GitHub CLI**

```bash
# En Windows (usando winget)
winget install --id GitHub.cli

# En macOS (usando Homebrew)
brew install gh

# En Linux (usando apt)
sudo apt install gh
```

---

### 🔐 **Autenticación**

```bash
# Iniciar sesión en GitHub
gh auth login
```

---

### 📦 **Crear un Nuevo Repositorio**

```bash
# Crear un nuevo repositorio en GitHub
gh repo create MiProyecto --public --source=. --remote=origin
```

---

### 📂 **Clonar un Repositorio**

```bash
# Clonar un repositorio existente
gh repo clone Usuario/MiProyecto
```

---

### 📝 **Gestionar Issues**

```bash
# Listar issues
gh issue list

# Crear un nuevo issue
gh issue create --title "Título del issue" --body "Descripción del issue"
```

---

### 🔄 **Gestionar Pull Requests**

```bash
# Listar pull requests
gh pr list

# Crear un nuevo pull request
gh pr create --title "Título del PR" --body "Descripción del PR" --base main --head feature/nueva-funcionalidad

# Fusionar un pull request
gh pr merge <ID-PR>
```

---

### 📊 **Verificar Estado del Repositorio**

```bash
# Verificar el estado del repositorio
gh repo view
```

---

### 🌟 **Flujo Completo de Desarrollo con GitHub CLI**

```bash
# 1️⃣ Clonar el repositorio
gh repo clone Usuario/MiProyecto

# 2️⃣ Crear una nueva rama para tu tarea
git checkout -b feature/nueva-funcionalidad

# 3️⃣ Hacer cambios y confirmar
git add .
git commit -m "Implementar nueva funcionalidad"

# 4️⃣ Subir la rama al repositorio remoto
git push origin feature/nueva-funcionalidad

# 5️⃣ Crear un Pull Request
gh pr create --title "Implementar nueva funcionalidad" --body "Descripción de los cambios" --base main --head feature/nueva-funcionalidad

# 6️⃣ Resolver conflictos (si los hay)
git merge origin/main
```

---

### **⚡ Consejos para Evitar Conflictos**
- **Comunicación:** Asegúrate de que todos los miembros trabajen en ramas separadas.  
- **Actualización constante:** Haz `git pull` regularmente antes de realizar cambios importantes.  
- **Revisión de PRs:** Usa Pull Requests para revisar el código antes de fusionar.

---

**🎉 ¡Feliz codificación! 🚀**