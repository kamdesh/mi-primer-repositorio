# Proyecto 01 - Uso básico de Git y GitHub

## Comandos de la guía

```bash
git init
git status
git add app.js
git commit -m "primer commit"
git config --global user.name
git config --global user.email
git log
git log --oneline
git diff HEAD~1 HEAD
git checkout <hash del primer commit>
git checkout main
git remote add origin <URL>
git remote -v
git push -u origin main
git pull
```

## Explicación breve

- `git init`: inicializa un repositorio Git en la carpeta actual.
- `git status`: muestra el estado de los archivos; permite ver cambios pendientes y el archivo modificado.
- `git add app.js`: prepara el archivo para el siguiente commit.
- `git commit -m "primer commit"`: guarda una instantánea del proyecto con el mensaje indicado.
- `git config --global user.name` y `git config --global user.email`: configuran la identidad del autor para futuros commits. En Windows y VS Code, se usa la terminal integrada; usa placeholders como TU-USUARIO y tu@email.com en lugar de los datos reales.
- `git log`: muestra el historial completo de commits.
- `git log --oneline`: resume el historial en una sola línea por commit.
- `git diff HEAD~1 HEAD`: compara el último commit con el anterior para ver cambios.
- `git checkout <hash del primer commit>`: permite moverse a un commit anterior para revisar el proyecto en ese punto.
- `git checkout main`: vuelve a la rama principal del proyecto.
- `git remote add origin <URL>`: conecta el repositorio local con un repositorio remoto en GitHub.
- `git remote -v`: lista la configuración de los remotos.
- `git push -u origin main`: sube la rama main al repositorio remoto y deja la relación de seguimiento.
- `git pull`: descarga cambios del remoto y los integra con el repositorio local.

## Salida esperada

- Se ve una carpeta `.git` en la raíz del proyecto.
- `git status` aparece limpio después del commit.
- `git log` y `git log --oneline` muestran el historial del proyecto.
- `git diff HEAD~1 HEAD` muestra el cambio entre el primer y el segundo estado del archivo.
- `git remote -v` muestra la URL de GitHub asociada.

## Capturas que debo tomar

- Actividad 1: carpeta `.git` creada.
- Actividad 2: primer commit realizado.
- Actividad 3: nuevo commit con el cambio de `app.js`.
- Actividad 4: cuenta de GitHub.
- Actividad 5: proyecto publicado en GitHub.
- Actividad 6: versiones sincronizadas.

## [ADICIONAL] Errores comunes

- Si aparece "Author identity unknown", se debe configurar nombre y correo con `git config --global user.name` y `git config --global user.email`.
- Si después de `git checkout <hash del primer commit>` se ve un aviso de "detached HEAD", significa que estás revisando un commit anterior. Para volver a la rama principal, usa `git checkout main`.
- Si la rama del repositorio es `master` en lugar de `main`, hay que crear o cambiar a `main` antes de subir.
