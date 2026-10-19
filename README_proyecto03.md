# Proyecto 03 - Landing page personal

## Comandos de la guía

```bash
git status
git add .
git commit -m "Agrega estructura HTML inicial"
git status
git add .
git commit -m "Agrega estilos básicos"
git status
git add .
git commit -m "Actualiza mensaje principal"
git status
git add .
git commit -m "Agrega footer"
git status
git add .
git commit -m "Agrega botón principal"
git status
git add .
git commit -m "Agrega animaciones básicas"
git config --list
git checkout <hash>
git checkout main
git clone <URL>
git pull
```

## Explicación breve

- `git status`: muestra el estado actual del repositorio antes de cada commit.
- `git add .`: agrega todos los cambios pendientes del proyecto al área de preparación.
- `git commit -m "..."`: guarda los cambios con un mensaje claro y descriptivo.
- `git config --list`: muestra la configuración global y local del entorno Git.
- `git checkout <hash>`: revisa un commit anterior para inspeccionar una versión del proyecto.
- `git checkout main`: vuelve a la rama principal.
- `git clone <URL>`: crea una copia local del repositorio desde GitHub.
- `git pull`: descarga y fusiona los cambios del remoto con la copia local.

## Código base

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8">
    <title>Mi Web</title>
  </head>
  <body>
    <h1>Hola Mundo</h1>
  </body>
</html>
```

```css
body { font-family: Arial; background: #f4f4f4; text-align: center; }
```

```html
<link rel="stylesheet" href="style.css">
```

```javascript
console.log("Mi Web");
```

```html
<script src="script.js"></script>
```

## Cambios adicionales de la guía

- Título actualizado:

```html
<h1>Bienvenido a mi sitio web</h1>
```

- Cambio sin commit para `git diff`:

```css
h1 { color: blue; }
```

- Se incorpora footer, botón principal y animación básica para completar la landing page.

## Salida esperada

- El historial del repositorio tiene commits con los mensajes indicados.
- `git status` muestra un árbol limpio al terminar cada commit.
- `git diff` permite ver el cambio de color de `h1` antes de confirmar el cambio.
- `git checkout <hash>` permite moverse entre versiones del proyecto.
- `git clone` crea otra copia del proyecto para simular dos computadoras.
- `git pull` sincroniza el repositorio remoto con la copia local.

## Capturas que debo tomar

- Estado inicial del proyecto antes del primer commit.
- Resultado de `git add .` y `git commit -m "Agrega estructura HTML inicial"`.
- Resultado de `git add .` y `git commit -m "Agrega estilos básicos"`.
- Resultado de `git add .` y `git commit -m "Actualiza mensaje principal"`.
- Resultado de `git add .` y `git commit -m "Agrega footer"`.
- Resultado de `git add .` y `git commit -m "Agrega botón principal"`.
- Resultado de `git add .` y `git commit -m "Agrega animaciones básicas"`.
- Estado de `git diff` con el cambio sin commit de `h1 { color: blue; }`.
- Resultado de `git config --list`.
- Resultado de `git checkout <hash>` y luego `git checkout main`.
- Resultado de `git clone` y `git pull` en la segunda computadora.

## [ADICIONAL] Notas de uso

- El comando `git diff` sin commit compara el contenido actual con el último estado guardado.
- Si luego de `git checkout <hash>` aparece "detached HEAD", esto es normal; solo indica que estás revisando un commit concreto. Para continuar el trabajo, usa `git checkout main`.
- En la práctica, para simular dos computadoras se puede clonar el repositorio en una segunda carpeta y luego hacer cambios en una de ellas antes de hacer `git pull`.
