# Mis Apuntes de Git

Guía rápida de comandos de terminal y Git para el manejo de proyectos.

---

## Comandos de Terminal (Navegación)
* `pwd` - Muestra la ruta de la carpeta donde estás parado.
* `ls` - Lista los archivos y carpetas del directorio actual.
* `cd [nombre]` - Entra en una carpeta.
* `cd ..` - Sube un nivel (vuelve a la carpeta anterior).
* `mkdir [nombre]` - Crea una carpeta nueva.
* `touch [archivo]` - Crea un archivo nuevo (ej: touch index.html).
* `code .` - Abre la carpeta actual en Visual Studio Code.

---

## Configuración e Inicio
* `git config --global user.name "Tu Nombre"` - Configura tu usuario para todo el equipo.
* `git init` - Arranca el control de versiones (crea la carpeta oculta .git).
* `git branch -m main` - Cambia el nombre de la rama principal a main.
* `git status` - Te dice cómo está el proyecto (qué archivos cambiaste o agregaste).

---

## Ciclo de Trabajo (Agregar y Guardar)
* `git add [archivo]` - Agrega un archivo específico al área de preparación.
* `git add .` - Agrega todos los cambios que tengas pendientes.
* `git commit -m "mensaje"` - Guarda los cambios con un comentario descriptivo.
* `git diff` - Muestra las diferencias entre el último commit y lo que tenés ahora.

---

## Historial y Recuperación
* `git log` - Muestra el historial de commits realizados.
* `git checkout [hash]` - Te lleva al estado del proyecto en ese hash específico.
* `git checkout [archivo]` - Vuelve el archivo a su estado en el último commit.
* `git reset --hard [hash]` - Ojo: Borra todos los commits posteriores y te deja el proyecto igual a ese hash.
* `git reflog` - Historial completo de interacciones (sirve para recuperar cosas borradas con reset hard).
* `git revert [hash]` - Deshace los cambios de un commit creando uno nuevo (no borra el historial).

---

## Ramas y Etiquetas
* `git branch [nombre]` - Crea una rama nueva (ej: git branch login).
* `git tag [nombre]` - Etiqueta el commit actual (se usa para marcar versiones como v1.0).

---

## Alias Personalizados
Para ver el historial de forma gráfica y resumida, podés configurar este comando:
```bash
git config --global alias.tree "log --graph --decorate --all --oneline"