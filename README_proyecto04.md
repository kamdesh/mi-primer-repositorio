# Proyecto 04 - Suma de 2 números

## Comandos de la guía

```bash
git init
git status
git add .
git commit -m "HTML base y primer commit"
git status
git add .
git commit -m "Formulario y CSS"
git status
git add .
git commit -m "JavaScript"
git diff
# error simulado: cambiar Number(num2.value) por num2.value
git diff
git add .
git commit -m "Corrige suma"
git push
```

## Explicación breve

- `git init`: crea el repositorio local.
- `git status`: revisa el estado del proyecto.
- `git add .`: agrega los archivos al área de preparación.
- `git commit -m "HTML base y primer commit"`: guarda la primera versión del sumador.
- `git commit -m "Formulario y CSS"`: guarda la versión con el formulario y estilo.
- `git commit -m "JavaScript"`: guarda la lógica del cálculo.
- `git diff`: permite comparar cambios actuales antes de confirmar.
- Error simulado: cambiar `Number(num2.value)` por `num2.value` provoca concatenación en lugar de suma porque JavaScript trata el contenido del input como texto.
- `git diff`: vuelve a mostrar el cambio para verificar el problema.
- `git add .` y `git commit -m "Corrige suma"`: corrigen el error y guardan la solución.
- `git push`: sube el proyecto al repositorio remoto.

## Código base final

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sumador</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <div class="container">
      <h1>Sumador</h1>
      <input id="num1" type="number" placeholder="Número 1">
      <input id="num2" type="number" placeholder="Número 2">
      <button id="sumBtn">Sumar</button>
      <h2 id="result">Resultado: 0</h2>
    </div>
    <script src="script.js"></script>
  </body>
</html>
```

```css
body {
  font-family: Arial, sans-serif;
  background: #f4f4f4;
  display: flex;
  justify-content: center;
  margin-top: 50px;
}

.container {
  background: white;
  padding: 20px;
  border-radius: 10px;
  width: 300px;
}

input,
button {
  width: 100%;
  margin-top: 10px;
  padding: 10px;
}
```

```javascript
const num1 = document.getElementById("num1");
const num2 = document.getElementById("num2");
const sumBtn = document.getElementById("sumBtn");
const result = document.getElementById("result");

sumBtn.addEventListener("click", () => {
  const total = Number(num1.value) + Number(num2.value);
  result.textContent = `Resultado: ${total}`;
});
```

## Salida esperada

- El proyecto muestra un formulario con dos inputs y un botón para sumar.
- Si se escribe 5 y 3 y se presiona "Sumar", la salida será `Resultado: 8`.
- Si se elimina `Number(...)`, la salida puede ser `Resultado: 53` porque se concatena como texto.
- El historial de Git refleja cada etapa: HTML base, formulario y CSS, JavaScript y corrección final.

## Capturas que debo tomar

- Estado inicial del repositorio y primer commit.
- Estado tras formulario y CSS.
- Estado tras lógica JavaScript.
- Detección del error con `git diff`.
- Corrección del error y commit final.
- Subida a GitHub con `git push`.

## [ADICIONAL] Por qué concatena

En JavaScript, si un valor viene de un input, normalmente se toma como cadena de texto. Al hacer `num2.value` sin convertir a número, el operador `+` puede unir cadenas, por eso `"5" + "3"` produce `"53"`. El uso de `Number(...)` fuerza la conversión a número antes de sumar.
