# IIDE · Horarios

App de horarios del Instituto Integral de Educación (Nivel Terciario), lista para publicar en GitHub Pages e instalar en el celular como una app.

## 📦 Qué hay en esta carpeta

- `index.html` — la app completa (no necesita instalación de nada, ni Node, ni npm).
- `manifest.json` — permite que el celular la instale como app.
- `sw.js` — hace que funcione offline (guarda una copia local).
- `icons/` — el ícono de la app en varios tamaños.

## 🚀 Paso 1: Subir a GitHub

1. Andá a [github.com](https://github.com) y creá una cuenta si no tenés.
2. Hacé clic en **"New repository"** (Nuevo repositorio).
3. Poné un nombre, por ejemplo `iide-horarios`. Dejalo **público**. No marques "Add a README" (ya tenemos uno).
4. Creá el repositorio.
5. En tu computadora, abrí una terminal en esta carpeta y ejecutá:

```bash
git init
git add .
git commit -m "Primera versión de la app de horarios"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/iide-horarios.git
git push -u origin main
```

(Reemplazá `TU-USUARIO` por tu usuario de GitHub y `iide-horarios` por el nombre que le pusiste al repositorio.)

> Si no tenés `git` instalado, también podés subir los archivos arrastrándolos directamente desde la página de GitHub, con el botón **"Add file" → "Upload files"**.

## 🌐 Paso 2: Activar GitHub Pages (para tener un link público)

1. En tu repositorio de GitHub, andá a **Settings** (Configuración).
2. En el menú de la izquierda, hacé clic en **Pages**.
3. En "Source", elegí la rama `main` y la carpeta `/ (root)`.
4. Guardá. GitHub te va a dar un link parecido a:

```
https://TU-USUARIO.github.io/iide-horarios/
```

Puede tardar 1-2 minutos en estar listo.

## 📱 Paso 3: Instalar en tu celular

Abrí ese link en el celular (Safari en iPhone, Chrome en Android):

**iPhone (Safari):**
1. Tocá el botón de **Compartir** (el cuadrado con la flecha hacia arriba).
2. Elegí **"Agregar a pantalla de inicio"**.
3. Confirmá. Va a aparecer como una app más, con el ícono del instituto.

**Android (Chrome):**
1. Tocá los tres puntos (⋮) arriba a la derecha.
2. Elegí **"Instalar app"** o **"Agregar a pantalla de inicio"**.
3. Confirmá.

Listo — la app queda instalada con su propio ícono, abre en pantalla completa (sin la barra del navegador), y sigue funcionando aunque no tengas internet en ese momento (usa la última versión guardada).

## 🔄 Cómo actualizar la app más adelante

Cada vez que quieras cambiar algo (por ejemplo, nuevos horarios el próximo cuatrimestre):
1. Reemplazá `index.html` por la nueva versión.
2. Volvé a subirlo a GitHub (`git add .` → `git commit` → `git push`, o subiendo el archivo de nuevo desde la web).
3. GitHub Pages se actualiza solo en 1-2 minutos. La próxima vez que la persona abra la app instalada, va a bajar la nueva versión automáticamente.

## ℹ️ Notas técnicas

- La app no necesita instalar nada (no usa Node.js ni npm) — es HTML, CSS y JavaScript que corre directo en el navegador, usando React vía CDN.
- Las aulas y profesores que editen los usuarios se guardan en la memoria del propio celular/navegador (`localStorage`), no se comparten automáticamente entre distintos dispositivos. Si más adelante querés que los cambios se vean en todos los celulares en tiempo real, hace falta agregar un backend (por ejemplo Firebase); avisame si querés que lo armemos.
