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

# Awesome Git

Una lista curada de herramientas, recursos y cosas brillantes de Git.

## Contribuyendo

Las solicitudes de extracción sobre herramientas/proyectos/recursos interesantes son bienvenidas.

## Tabla de Contenidos

- [Awesome Git](#awesome-git)
  - [Tutorial](#tutorial)
  - [Guía de Estilo](#guía-de-estilo)
  - [Cliente](#cliente)
  - [Alojamiento de Repositorios](#alojamiento-de-repositorios)
  - [Repositorio Autoalojado](#repositorio-autoalojado)
  - [Flujo de Trabajo](#flujo-de-trabajo)
  - [Gestión de Hooks](#gestión-de-hooks)
  - [Herramientas](#herramientas)
  - [Extensiones](#extensiones)

## Tutorial

*Hay toneladas de material de aprendizaje en la Web*

* [Try Git](https://try.github.io/) - aprende Git en 15 minutos con una interfaz pseudo-terminal
* [Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials/) - tutorial completo sobre Git
* [Learn Version Control with Git](https://www.git-tower.com/learn/) - libro freemium de fournova Software (creadores de Tower), asociado con un curso de video pago
* [Pro Git](https://git-scm.com/book/) - libro gratuito de Git, también disponible en papel (CC BY-NC-SA 3.0)
* [Learn how to use Git](https://www.deployhq.com/git) - tutoriales y recursos gratuitos para ayudarte a aprender los conceptos básicos de Git
* [The Git Community Book](https://schacon.github.io/gitbook/) - libro construido por docenas de personas en la comunidad Git
* [Git Pocket Guide](https://shop.oreilly.com/product/0636920024972) - un libro corto de O'Reilly sobre Git
* [Git Real: Code School](https://www.codeschool.com/courses/git-real/) - curso de formación pago de Code School
* [Git Branching](https://pcottle.github.io/learnGitBranching/) - forma visual de aprender ramificación en git
* [Learn Git in a Month of Lunches](https://www.manning.com/books/learn-git-in-a-month-of-lunches) - libro basado en tutoriales de Manning Publications
* [Git Magic](http://www-cs-students.stanford.edu/~blynn/gitmagic/index.html) - libro corto sobre Git
* [Git from the bottom up](https://jwiegley.github.io/git-from-the-bottom-up/) - gran serie de artículos sobre Git
* [Git-It](https://github.com/jlord/git-it-electron) - Aplicación de Tutorial Interactivo que se ejecuta en tu Escritorio
* [Git How To](https://githowto.com) - introducción paso a paso
* [Migrating to Git LFS](https://vooban.com/en/tips-articles-geek-stuff/migrating-to-git-lfs-for-developing-deep-learning-applications-with-large-files/) - Usa Git LFS en un repositorio existente para gestionar archivos grandes de una mejor manera
* [Explain Git with D3](https://onlywei.github.io/explain-git-with-d3/) - Conceptos básicos de Git visualizados usando D3.js: commit, branch, checkout, reset, revert, merge, rebase, fetch, pull, push, tag
* [Making Sense of Git – A Visual Perspective](https://appendto.com/2015/06/making-sense-of-git-a-visual-perspective/) - Git desde una perspectiva de línea de tiempo y nivel y hoja de trucos de comandos de git agrupados por funcionalidad
* [Git &amp; Git-Flow Cheat Sheet](https://github.com/arslanbilal/git-cheat-sheet)
* [Git Tips](https://github.com/git-tips/tips)
* [Interactive/Contextual/Visual Cheat Sheet](https://ndpsoftware.com/git-cheatsheet.html)
* [The &#39;Git Pretty&#39; Flow-Chart](http://justinhileman.info/article/git-pretty/git-pretty.png) - Cómo Recuperarse de un Desastre
* [Software Carpentry: Git Lessons](https://software-carpentry.org/lessons/)
* [The Git Parable](http://tom.preston-werner.com/2009/05/19/the-git-parable.html) - Introducción narrativa a los conceptos de Git por el cofundador de GitHub
* [CodeBasicsHub: Git Video Tutorials](https://codebasicshub.com/tutorial/git-github/what-is-git)
* [Intermediate Git](http://www.columbia.edu/~zjn2101/intermediate-git/#1) - explicación más estructural y de bajo nivel de los conceptos de git
* [Fork and Pull Request Workflow](https://github.com/susam/gitpr) - Forma muy bien explicada, simple y concisa de entender el flujo de trabajo de fork y pull request en git.
* [Git School Dude](https://www.youtube.com/c/DanGitschoolDude) - Es un canal de YouTube con muchos videos geniales sobre git. Cubre todo, desde los conceptos básicos hasta temas avanzados de Git.
* [A Git Choose Your Own Adventure](https://sethrobertson.github.io/GitFixUm/fixup.html) - Nunca encontré un tutorial de git que no entendiera mientras lo hacía. Solo que a veces esos tutoriales no se alineaban muy bien con mi trabajo real. Esta ayuda de git en forma de elige tu propia aventura fue un salvavidas cuando recién comenzaba.
* [On undoing, fixing, or removing commits in git](https://sethrobertson.github.io/GitFixUm/fixup.html) - guía bastante completa sobre cómo recuperarse de lo que no querías hacer al usar git
* [Deconstructing a git commit](https://krishnabiradar.com/blogs/deconstructing-a-git-commit/) - Un blog que explica cómo git crea y almacena historiales de commits.
* [Flight rules for Git](https://github.com/k88hudson/git-flight-rules) - guía sobre qué hacer cuando las cosas salen mal
* [Use gitk to understand git](https://lostechies.com/joshuaflanagan/2010/09/03/use-gitk-to-understand-git/) - todos los términos importantes de Git (commit, commit SHA, branch, merge, rebase) explicados usando gitk
* [Git Cherry-pick and its usages](https://www.loginradius.com/blog/async/git-cherry-pick/) - Un blog que explica cómo funciona el comando git cherry-pick.
* [The ultimate guide to `<code>`.gitignore`</code>`](https://github.com/groda/the_ultimate_gitignore_guide) Todo sobre `.gitignore`.
* [No Bullsh\*t Git](https://maciejb2k.github.io/no-bs-git/) - explicación gratuita y completa de los internos de git y el directorio `.git/`.

## Guía de Estilo

*Guía de estilo cuando trabajas con git*

* [Udacity Nanodegree Style Guide](https://udacity.github.io/git-styleguide/index.html)

## Cliente

*Los clientes de Git están disponibles en todas las plataformas, desde mainframes hasta tu dispositivo móvil*

* [GitHub Desktop](https://desktop.github.com/) - Cliente Git de GitHub. Funciona perfectamente con GitHub y GitHub Enterprise.
* [SourceTree](https://www.sourcetreeapp.com/) - Cliente GUI gratuito (in-beer). Solo para Windows y Mac.
* [Tower](https://www.git-tower.com/) - Un popular cliente GUI de Git no gratuito. Mac y Windows.
* [GitKraken](https://www.gitkraken.com/) - Un cliente Git multiplataforma para Windows, Mac y Linux. Basado en Electron. Gratis para uso no comercial y versión Pro de pago disponible.
* [Fork](https://git-fork.com) - Un cliente Git impresionante y gratuito para macOS y Windows.
* [TortoiseGit](https://tortoisegit.org/) - Un cliente Git fácil de usar en Windows. Bien integrado con el Explorador de Windows.
* [SmartGit](https://www.syntevo.com/smartgit/) - Un cliente SCM comercial integral con Git, SVN, Mercurial. Multiplataforma (funciona en Windows, Mac y Linux).
* [RabbitVCS](http://rabbitvcs.org/) - Herramienta gráfica inspirada en TortoiseSVN para sistemas de control de versiones, con integración en Nautilus y Thunar.
* [gitg](https://wiki.gnome.org/Apps/Gitg/) - Un cliente GUI de código abierto basado en GTK+.
* [git-cola](https://git-cola.github.io/) - Un cliente GUI de Git multiplataforma.
* [SGit](https://github.com/sheimi/SGit) - Cliente Git para Android 4.x.
* [Ungit](https://github.com/FredrikNoren/ungit) - La forma más fácil de usar git. En cualquier plataforma. En cualquier lugar.
* [GitUp](http://gitup.co) - Un cliente Git limpio y minimalista. Solo para Mac.
* [GitExtensions](https://gitextensions.github.io/) - Una extensión de shell, un plugin para Visual Studio 2010-2015 y una herramienta independiente para repositorios Git.
* [WorkingCopy](https://workingcopyapp.com) - Un potente cliente Git para iOS. Gratis con compra dentro de la aplicación para desbloquear la capacidad de enviar commits.
* [Git Add-ons](https://github.com/stevemao/awesome-git-addons) - Mejora el CLI básico de `git`.
* [Magit](https://magit.vc) - Una porcelana de Git dentro de Emacs.
* [Vershd](https://vershd.io/) - Un GUI de Git sin esfuerzo y gratuito para uso personal en Windows, Mac y Linux.
* [lazygit](https://github.com/jesseduffield/lazygit) - Una interfaz de usuario simple para terminal para comandos git, escrita en Go.
* [Gittyup](https://github.com/Murmele/Gittyup) - Un cliente gráfico de Git diseñado para ayudarte a entender y gestionar el historial de tu código fuente.

## Alojamiento de Repositorios

*Las personas tienen muchas opciones para alojar su código fuente*

* [GitHub](https://github.com/) - El servicio de alojamiento git por defecto. Integración perfecta con la mayoría de los servicios externos.
  * [Awesome GitHub](https://github.com/phillipadsmith/awesome-github) - Recursos y aprendizaje para GitHub.
    * [GitHub Cheat Sheet](https://github.com/tiimgreen/github-cheat-sheet)
    * [GitHub Browser Extensions](https://github.com/stefanbuck/awesome-browser-extensions-for-github)
* [BitBucket](https://bitbucket.org/) - Conocido por su repositorio privado gratuito (máximo 5 usuarios).
* [Jetbrains Space](https://www.jetbrains.com/space/) - Solución todo en uno de Jetbrains para equipos de software, con IM, seguimiento de tickets, control de versiones.
* [GitLab.com](https://about.gitlab.com/gitlab-com/) - Un servicio gratuito de alojamiento de repositorios Git servido por GitLab EE. Repositorios ilimitados y colaboradores privados.
* [Azure DevOps](https://azure.microsoft.com/en-us/services/devops/) - Servicio en la nube para desarrollo de software anteriormente conocido como Visual Studio Team Services, Visual Studio Online y Team Foundation Service Preview.
* [AWS CodeCommit](https://aws.amazon.com/codecommit/) - Un servicio SaaS proporcionado por Amazon Web Service en una infraestructura de alta disponibilidad.
* [Kiln](https://www.fogcreek.com/kiln/) - Servicio de alojamiento de repositorios Git de pago.
* [Deveo](https://deveo.com/) - Un servicio de alojamiento de repositorios de pago con soporte para Git, Subversion, Mercurial, WebDAV.

## Repositorio Autoalojado

*O puedes alojar el código tú mismo*

* [Gitolite](https://gitolite.com/gitolite/) - Simple con control de acceso detallado.
* [GitHub Enterprise](https://enterprise.github.com/) - Solución autoalojada proporcionada por GitHub.
* [Bitbucket Server](https://www.atlassian.com/software/bitbucket/server) - Solución autoalojada de Atlassian. Buena integración con JIRA y otros productos de Atlassian.
* [GitLab CE/EE](https://gitlab.com/) - Un popular Git de código abierto (CE) con opción de soporte de pago (EE).
* ~~[Upsource](https://www.jetbrains.com/upsource) - Oferta reciente de Jetbrains, una famosa empresa de software orientada a desarrolladores. Función de alojamiento de repositorios pendiente. Gratis para 10 usuarios. Buena integración con YouTrack y TeamCity~~
  * Upsource ya no está disponible como producto comercial desde el 1 de febrero de 2022.[*](https://www.jetbrains.com/upsource/)
* [Gogs](https://gogs.io/) - Un servicio Git autoalojado escrito en Go.
* [Gitea](https://gitea.io/) - Un fork gestionado por la comunidad de Gogs, solución ligera de alojamiento de código escrita en Go.
* [onedev](https://github.com/theonedev/onedev) - Servidor Git autoalojado con Kanban y CI/CD.
* [GitBucket](https://github.com/takezoe/gitbucket/) - Un clon de GitHub impulsado por Scala.
* [GitBlit](http://gitblit.com/) - Pila Java pura para gestionar, ver y servir repositorios Git.
* [Apache Allura](https://allura.apache.org/) - Una implementación de código abierto de una plataforma de alojamiento de proyectos.
* [Phabricator](https://www.phacility.com/) - Un conjunto integrado de herramientas poderosas para ayudar a las empresas a construir software de mayor calidad.
  * A partir del 1 de junio de 2021: Phabricator ya no se mantiene activamente.[*](https://admin.phacility.com/phame/post/view/11/phacility_is_winding_down_operations/)
* [RhodeCode CE/EE](https://rhodecode.com/) - Una plataforma que ofrece gestión de código fuente empresarial.
* [Soft Serve](https://github.com/charmbracelet/soft-serve) - Un sabroso servidor Git autoalojado para la línea de comandos.

## Flujo de Trabajo

*La ramificación económica permite a las personas adoptar flujos de trabajo diferentes al flujo de trabajo centralizado clásico*

* [Pro Git - Flujos de Trabajo Distribuidos](https://git-scm.com/book/it/v2/Distributed-Git-Distributed-Workflows)
* [Atlassian Git Tutorial - Comparación de Flujos de Trabajo](https://www.atlassian.com/git/tutorials/comparing-workflows)
* [Patrones para Gestionar Ramas de Código Fuente](https://martinfowler.com/articles/branching-patterns.html)
* [Artículo de Modelos de Ramificación de Nyx](https://mooltiverse.github.io/nyx/guide/user/best-practice/branching-models/)

### Comparación de flujos de trabajo

*Ningún flujo de trabajo único se adapta a las necesidades de todos*

* [Gitflow](https://nvie.com/posts/a-successful-git-branching-model/) - el modelo de flujo de trabajo Git más conocido
* [GitHub flow](http://scottchacon.com/2011/08/31/github-flow.html) - un modelo de ramificación simple con un solo master
* [GitLab flow](https://about.gitlab.com/2014/09/29/gitlab-flow/)
* [Git DMZ Flow](https://gist.github.com/djspiewak/9f2f91085607a4859a66)
* [Aoneflow](https://www.alibabacloud.com/blog/how-do-we-manage-code-branches-at-alibaba_593834) - un modelo de rama interesante que retrasa la fusión final a la rama de producción, adoptado por Alibaba. más artículos (en texto chino) en [1](https://segmentfault.com/a/1190000016373314), [2](https://yq.aliyun.com/articles/573549)
* [Agit-flow](https://git-repo.info/en/2020/03/agit-flow-and-git-repo/) - Inspirado en el flujo de trabajo de Gerrit, Agit-flow es un flujo de trabajo git centralizado y se utiliza en la plataforma de código fuente interna de Alibaba

## Gestión de Hooks

*Git proporciona hooks en la fase de commit/push, permitiendo la integración con herramientas de verificación de calidad de código y Continuous Integration (CI)*

* [pre-commit](https://pre-commit.com) - un marco para gestionar y mantener hooks pre-commit multilenguaje.
* [husky](https://github.com/typicode/husky) - hooks de Git modernos y nativos hechos fáciles.
* [Overcommit](https://github.com/brigade/overcommit) - un gestor de hooks de Git extensible escrito en Ruby.
* [lefthook](https://github.com/evilmartians/lefthook) - gestor de hooks de Git rápido y potente para cualquier tipo de proyecto.
* [Mookme](https://github.com/Escape-Technologies/mookme) - Un hook de git simple y fácil de usar, pero poderoso y agnóstico al lenguaje para monorepos.
* [quickhook](https://github.com/dirk/quickhook) - un ejecutor de hooks de Git rápido y con estilo Unix.
* más en https://githooks.com/

## Herramientas

*Varias herramientas para operaciones diarias*

* [awesome-git-addons](https://github.com/stevemao/awesome-git-addons) - lista más de 20 complementos de git incluyendo todos los comandos disponibles
* [myrepos](https://myrepos.branchable.com/) - una herramienta para gestionar múltiples repositorios de control de versiones
* [mu-repo](https://fabioz.github.io/mu-repo/) - una herramienta para ayudar a manejar múltiples repositorios git
* [multi-gitter](https://github.com/lindell/multi-gitter) - una herramienta para hacer cambios en múltiples repositorios simultáneamente
* [gitwalk](https://github.com/pazdera/gitwalk) - Procesamiento masivo de repositorios git
* [gr](http://mixu.net/gr/) - una herramienta para gestionar múltiples repositorios git
* [BFG Repo-Cleaner](https://rtyley.github.io/bfg-repo-cleaner/) - una alternativa más simple y rápida a git-filter-branch para limpiar datos incorrectos del historial de tu repositorio Git
* [GitIgnore Collection](https://github.com/github/gitignore) - colección de archivos gitignore para varios lenguajes de programación
* [etckeeper](https://etckeeper.branchable.com/) - una colección de herramientas para permitir que /etc se almacene en un repositorio git
* [git-extras](https://github.com/tj/git-extras) – utilidades git que añaden comandos útiles a git.
* [git-extra-commands](https://github.com/unixorn/git-extra-commands) - Otra colección de comandos útiles de git.
* [git-follow](https://github.com/nickolasburr/git-follow) - una herramienta para seguir los cambios de por vida de un archivo a lo largo del historial de un repositorio Git.
* [Gitrob](https://github.com/michenriksen/gitrob) - una herramienta de línea de comandos para encontrar información sensible en archivos disponibles públicamente en GitHub
* [gitFS](https://www.presslabs.com/gitfs/) - un sistema de archivos FUSE que se integra completamente con git
* [Gitless](https://gitless.com/) - una versión experimental de Git que cambia algunos de los conceptos subyacentes de Git
* [ghq](https://github.com/motemen/ghq) — Organización para repositorios remotos
* [bash-git-prompt](https://github.com/magicmonty/bash-git-prompt) - Un prompt de bash informativo y elegante para usuarios de Git
* [conventional-changelog](https://github.com/conventional-changelog/conventional-changelog) - un conjunto de herramientas para analizar mensajes de commit convencionales del historial de git
* [release-it](https://github.com/webpro/release-it) - Automatiza lanzamientos para repositorios Git y/o paquetes npm. Generación de changelog, lanzamientos en GitHub/GitLab, etc.
* [gickup](https://github.com/cooperspencer/gickup) - Respaldo de repositorios desde varios hosters a local u otros hosters.
* [git-absorb](https://github.com/tummychow/git-absorb) - `git commit --fixup`, pero automático
* [jc --git-log](https://kellyjonbrazil.github.io/jc/docs/parsers/git_log) - Convierte tu git log a JSON.
* [gitbackup](https://github.com/amitsaha/gitbackup) - una herramienta para respaldar tus repositorios de Bitbucket, GitHub y GitLab.
* [soba](https://github.com/jonhadfield/soba) - respaldos programados de repositorios de proveedores populares con detección de cambios.
* [tig](https://github.com/jonas/tig) - interfaz de modo texto para git.

## Extensiones

*Git está diseñado para la gestión del control de versiones del código fuente, pero las personas extienden la idea y llevan el control de versiones a todas partes*

* [Git Large File Storage](https://git-lfs.github.com/) - practical solution for versioning large files. supported by GitHub
* [Git Virtual File System or GVFS](https://github.com/Microsoft/GVFS) - solution for managing very large Git repository while maintaining speed and efficiency of most operations. in developement by Microsoft.
* [git-annex](https://git-annex.branchable.com/) - allow managing large binaries among machines, as if operation a normal git repository. possible to creates a synchronised folder with [git-annex assistant](https://git-annex.branchable.com/assistant/).
