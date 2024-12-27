# 📝 **Git y GitHub Cheatsheet: Flujo Completo de Desarrollo**

---

## 🚀 **Configuración Inicial del Repositorio**

1️⃣ Inicializar un repositorio local
```bash
git init
```

2️⃣ Configurar identidad global (si no está configurado)
```bash
git config --global user.name "TuNombre"
git config --global user.email "TuCorreo@example.com"
```

3️⃣ Crear un archivo README.md o cualquier archivo inicial
```bash
echo "# MiProyecto" > README.md
```

4️⃣ Agregar todos los archivos al área de preparación (staging)
```bash
git add .
```

5️⃣ Realizar el primer commit
```bash
git commit -m "Primer commit: inicialización del proyecto"
```

6️⃣ Crear un repositorio remoto en GitHub
- Desde GitHub, crea un nuevo repositorio y copia la URL.

7️⃣ Vincular el repositorio local con el remoto
```bash
git remote add origin https://github.com/Usuario/MiProyecto.git
```

8️⃣ Subir los cambios iniciales al repositorio remoto
```bash
git branch -M main    # Renombrar la rama a 'main', si no existe
git push -u origin main
```

---

## 📂 **Flujo de Trabajo Básico: Añadir, Confirmar y Subir Cambios**

1️⃣ Verificar estado del repositorio
```bash
git status
```

2️⃣ Agregar cambios al área de preparación
```bash
git add <archivo>          # Para un archivo específico
git add .                  # Para todos los archivos
```

3️⃣ Confirmar cambios con un mensaje
```bash
git commit -m "Descripción breve del cambio"
```

4️⃣ Subir los cambios al repositorio remoto
```bash
git push origin <rama>
```

---

## 🌿 **Gestión de Ramas (Branches)**

1️⃣ Crear una nueva rama
```bash
git branch <nombre-rama>
```

2️⃣ Cambiar a la nueva rama
```bash
git checkout <nombre-rama>
```

3️⃣ Crear y cambiar a una nueva rama en un solo paso
```bash
git checkout -b <nombre-rama>
```

4️⃣ Listar todas las ramas
```bash
git branch
```

5️⃣ Eliminar una rama local
```bash
git branch -d <nombre-rama>
```

---

## 🔄 **Fusionar Ramas (Merging)**

1️⃣ Cambiar a la rama destino (por ejemplo, main)
```bash
git checkout main
```

2️⃣ Fusionar la rama específica con la actual
```bash
git merge <nombre-rama>
```

3️⃣ Resolver conflictos (si ocurren)
- Editar archivos con conflictos, luego:
```bash
git add <archivo-con-resolucion>
git commit -m "Conflictos resueltos"
```

---

## ⬇️ **Actualizar el Repositorio Local (Pull)**

- Obtener y fusionar cambios del repositorio remoto
```bash
git pull origin <rama>
```

---

## 🔍 **Gestión de Historial y Restauración de Cambios**

1️⃣ Mostrar el historial de commits
```bash
git log                    # Ver historial completo
git log --oneline          # Ver historial resumido
```

2️⃣ Ver diferencias entre commits
```bash
git diff                   # Ver cambios no confirmados
git diff <commit1> <commit2>
```

3️⃣ Deshacer cambios
```bash
git restore <archivo>       # Restaurar un archivo al último commit
git restore --staged <archivo>  # Quitar un archivo del área de preparación
```

4️⃣ Resetear commits (con cuidado)
```bash
git reset --soft HEAD~1     # Mantener cambios en el área de preparación
git reset --mixed HEAD~1    # Mantener cambios en el directorio de trabajo
git reset --hard HEAD~1     # Deshacer todos los cambios y commits
```

---

## 🛠️ **Escenarios de Recuperación y Reparación de Commits**

1️⃣ Recuperar un commit eliminado
```bash
git reflog                  # Ver historial de referencias
git checkout <hash-commit>
```

2️⃣ Crear un commit nuevo corrigiendo el anterior
```bash
git commit --amend -m "Nuevo mensaje para el último commit"
```

3️⃣ Volver a un commit anterior sin borrar commits posteriores
```bash
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

1️⃣ Actualizar la rama local antes de trabajar
```bash
git pull origin main
```

2️⃣ Crear una rama nueva para tu tarea
```bash
git checkout -b feature/nueva-funcionalidad
```

3️⃣ Hacer cambios y confirmar
```bash
git add .
git commit -m "Implementar nueva funcionalidad"
```

4️⃣ Subir la rama al repositorio remoto
```bash
git push origin feature/nueva-funcionalidad
```

5️⃣ Crear un Pull Request desde GitHub

6️⃣ Resolver conflictos (si los hay)
```bash
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

- En Windows (usando winget)
```bash
winget install --id GitHub.cli
```

- En macOS (usando Homebrew)
```bash
brew install gh
```

- En Linux (usando apt)
```bash
sudo apt install gh
```

---

### 🔐 **Autenticación**

- Iniciar sesión en GitHub
```bash
gh auth login
```

---

### 📦 **Crear un Nuevo Repositorio**

- Crear un nuevo repositorio en GitHub
```bash
gh repo create MiProyecto --public --source=. --remote=origin
```

---

### 📂 **Clonar un Repositorio**

- Clonar un repositorio existente
```bash
gh repo clone Usuario/MiProyecto
```

---

### 📝 **Gestionar Issues**

- Listar issues
```bash
gh issue list
```

- Crear un nuevo issue
```bash
gh issue create --title "Título del issue" --body "Descripción del issue"
```

---

### 🔄 **Gestionar Pull Requests**

- Listar pull requests
```bash
gh pr list
```

- Crear un nuevo pull request
```bash
gh pr create --title "Título del PR" --body "Descripción del PR" --base main --head feature/nueva-funcionalidad
```

- Fusionar un pull request
```bash
gh pr merge <ID-PR>
```

---

### 📊 **Verificar Estado del Repositorio**

- Verificar el estado del repositorio
```bash
gh repo view
```

---

### 🌟 **Flujo Completo de Desarrollo con GitHub CLI**

1️⃣ Clonar el repositorio
```bash
gh repo clone Usuario/MiProyecto
```

2️⃣ Crear una nueva rama para tu tarea
```bash
git checkout -b feature/nueva-funcionalidad
```

3️⃣ Hacer cambios y confirmar
```bash
git add .
git commit -m "Implementar nueva funcionalidad"
```

4️⃣ Subir la rama al repositorio remoto
```bash
git push origin feature/nueva-funcionalidad
```

5️⃣ Crear un Pull Request
```bash
gh pr create --title "Implementar nueva funcionalidad" --body "Descripción de los cambios" --base main --head feature/nueva-funcionalidad
```

6️⃣ Resolver conflictos (si los hay)
```bash
git merge origin/main
```

---

### **⚡ Consejos para Evitar Conflictos**
- **Comunicación:** Asegúrate de que todos los miembros trabajen en ramas separadas.
- **Actualización constante:** Haz `git pull` regularmente antes de realizar cambios importantes.
- **Revisión de PRs:** Usa Pull Requests para revisar el código antes de fusionar.

---

**🎉 ¡Feliz codificación! 🚀**