# Proyecto 02 - Historial de un proyecto Node.js

## Comandos de la guía

```bash
mkdir proyecto02
cd proyecto02
git init
git status
git add tareas.js
git commit -m "primer commit"
# modificar tareas.js para la segunda versión
git status
git add tareas.js
git commit -m "segunda versión"
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

- `mkdir proyecto02` y `cd proyecto02`: crean la carpeta del proyecto y entran a ella.
- `git init`: inicializa el repositorio Git.
- `git status`: revisa el estado inicial del repositorio.
- `git add tareas.js`: agrega el archivo al área de preparación.
- `git commit -m "primer commit"`: guarda la primera versión del proyecto.
- Modificar `tareas.js` para la segunda versión: se agregan las tareas 1, 2 y 3.
- `git status`: confirma que hay cambios pendientes.
- `git add tareas.js`: prepara la segunda versión.
- `git commit -m "segunda versión"`: guarda el segundo avance del proyecto.
- `git log --oneline`: muestra un resumen del historial.
- `git diff HEAD~1 HEAD`: compara el primer y el segundo commit.
- `git checkout <hash del primer commit>`: revisa el proyecto como estaba en el pasado.
- `git checkout main`: vuelve al estado actual de la rama principal.
- `git remote add origin <URL>`: conecta el repositorio local con GitHub.
- `git remote -v`: muestra la URL configurada.
- `git push -u origin main`: sube el proyecto al repositorio remoto.
- `git pull`: sincroniza con los cambios del repositorio remoto.

## Salida esperada

- El repositorio tiene 2 commits principales: primero y segunda versión.
- `git log --oneline` muestra un listado breve con ambos commits.
- `git diff HEAD~1 HEAD` muestra claramente la diferencia entre la primera y segunda versión del archivo.
- Al usar `git checkout <hash>` se observa el estado del proyecto en un punto anterior.
- Al hacer `git checkout main` se vuelve al estado actual del proyecto.
- `git remote -v` muestra la URL de GitHub configurada correctamente.

## Capturas que debo tomar

- Crear proyecto y realizar `git init`.
- Hacer el primer commit.
- Modificar `tareas.js` para la segunda versión.
- Ver historial resumido con `git log --oneline`.
- Comparar primer y segundo commit con `git diff HEAD~1 HEAD`.
- Viajar al pasado con `git checkout <hash>`.
- Volver a `main` con `git checkout main`.
- Conectar a GitHub con `git remote add origin <URL>`.
- Realizar el primer push.
- Simular cambio remoto en GitHub y ejecutar `git pull`.

## [ADICIONAL] Observaciones

- Si el historial se ve vacío luego de `git checkout <hash>`, significa que estás en un commit aislado y no en la rama principal.
- Si `git pull` falla cuando se simuló un cambio en GitHub, puede deberse a que no hubo una rama o a que el remoto no estaba sincronizado. En la práctica se resuelve con `git pull origin main` y revisando el estado antes del merge.
