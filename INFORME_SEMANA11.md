# Informe Semana 11: Control de versiones y colaboración

## Datos del estudiante

- Nombre: _______________________________________________
- Carrera: ______________________________________________
- Grupo: _________________________________________________
- Fecha: _________________________________________________
- Profesor: ______________________________________________
- Curso: Desarrollo de Aplicaciones Web ____________________

## Objetivo

Aplicar los conceptos básicos de Git y GitHub para gestionar versiones, colaborar en proyectos y registrar el historial de trabajo con commits, ramas y sincronización con un repositorio remoto.

## Desarrollo por proyecto

### Proyecto 1 - Uso básico de Git y GitHub

#### Comandos

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

#### Resultado esperado

- Se crea un repositorio local con la carpeta .git.
- Se registra el primer commit.
- Se observa el historial con commits y cambios.
- Se conecta el proyecto con GitHub y se sincroniza la rama main.

#### Explicación breve

El flujo inicia con la inicialización del repositorio y la preparación del archivo app.js. Luego se realiza el primer commit, se revisa el historial y se comparan versiones. Con git checkout se puede volver a un estado anterior del proyecto, y con git remote, git push y git pull se conecta y sincroniza con GitHub. [INSERTAR CAPTURA AQUÍ]

---

### Proyecto 2 - Historial de un proyecto Node.js

#### Comandos

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

#### Resultado esperado

- El proyecto tiene dos versiones principales de tareas.js.
- Se observa el historial resumido y la diferencia entre commits.
- Se revierte temporalmente a una versión pasada y luego se regresa a main.
- Se sincroniza con GitHub y se actualiza con pull.

#### Explicación breve

Este proyecto demuestra cómo mantener el historial de un proyecto con cambios incrementales. Permite comparar versiones, revisar commits antiguos y simular cambios en GitHub para luego actualizar el repositorio local. [INSERTAR CAPTURA AQUÍ]

---

### Proyecto 3 - Landing page personal

#### Comandos

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

#### Resultado esperado

- El proyecto mantiene un historial limpio con mensajes de commit claros.
- La landing page evoluciona con estructura, estilo, texto principal, footer, botón y animaciones.
- Se pueden revisar versiones anteriores con git checkout y simular dos computadoras usando git clone y git pull.

#### Explicación breve

El flujo de trabajo se repite con git status, git add . y git commit -m "..." para guardar cambios de manera ordenada. El proyecto permite ver cómo un sitio web puede evolucionar de manera ordenada y cómo colaborar desde diferentes copias del repositorio. [INSERTAR CAPTURA AQUÍ]

---

### Proyecto 4 - Suma de 2 números

#### Comandos

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

#### Resultado esperado

- Se crea la estructura HTML base del sumador.
- Se agrega formulario con entradas y estilos.
- Se implementa la lógica de cálculo y se detecta un error de concatenación.
- Se corrige el problema y se sube el proyecto a GitHub.

#### Explicación breve

Este proyecto aplica Git en un caso real de depuración. El error de concatenación ocurre cuando se usa num2.value sin convertirlo a número, porque JavaScript interpreta los valores de entrada como texto. La corrección con Number(...) convierte ambos valores a numerales para realizar la suma correctamente. [INSERTAR CAPTURA AQUÍ]

---

## Conclusiones

El uso de Git permitió llevar un control ordenado del historial del proyecto, mantener copias seguras y facilitar la colaboración con GitHub. La práctica mostró la importancia de documentar cambios con commits claros, revisar el historial con git log y git diff, y usar checkout para volver a versiones previas cuando es necesario. También se comprendió la ventaja de mantener el repositorio en la rama main y sincronizarlo con el remoto mediante push y pull.

## Capturas requeridas

- [INSERTAR CAPTURA AQUÍ] Proyecto 1: carpeta .git y primer commit.
- [INSERTAR CAPTURA AQUÍ] Proyecto 1: nuevo commit y comparativa entre versiones.
- [INSERTAR CAPTURA AQUÍ] Proyecto 1: cuenta de GitHub y repositorio publicado.
- [INSERTAR CAPTURA AQUÍ] Proyecto 2: historial resumido y git diff entre commits.
- [INSERTAR CAPTURA AQUÍ] Proyecto 2: git checkout al pasado y regreso a main.
- [INSERTAR CAPTURA AQUÍ] Proyecto 3: historial con commits del sitio web.
- [INSERTAR CAPTURA AQUÍ] Proyecto 3: git clone y git pull desde la segunda computadora.
- [INSERTAR CAPTURA AQUÍ] Proyecto 4: detección del error de concatenación y corrección final.
- [INSERTAR CAPTURA AQUÍ] Proyecto 4: push final al repositorio remoto.

## [ADICIONAL] Recomendaciones

- Antes de usar Git por primera vez en Windows con VS Code, verificar la configuración de nombre y correo con git config --global user.name y git config --global user.email.
- Si aparece un aviso de Author identity unknown, completar la configuración.
- Si se usa git checkout <hash> y aparece detached HEAD, es normal; para continuar, volver a main con git checkout main.
- En caso de conflicto al hacer git pull, revisar los archivos modificados y resolverlo con cuidado antes de hacer commit.
