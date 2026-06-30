# Bitácora del Proyecto — Restaurante

Agenda/diario instalable (PWA) con un plan de 14 días para construir el menú del restaurante mientras aprendes a programar. Tiene racha y puntos: si no cierras el día, la racha se apaga y pierdes puntos.

## Cómo publicarla en GitHub Pages (gratis)

1. Crea un repositorio nuevo en GitHub (puede ser público), por ejemplo `bitacora-restaurante`.
2. Sube **todos** estos archivos a la raíz del repositorio (no en una subcarpeta):
   - `index.html`
   - `manifest.webmanifest`
   - `sw.js`
   - `icons/icon-192.png`
   - `icons/icon-512.png`
3. En el repositorio, ve a **Settings → Pages**.
4. En "Branch", selecciona `main` (o `master`) y carpeta `/ (root)`. Guarda.
5. Espera 1-2 minutos. GitHub te dará una URL parecida a:
   `https://tu-usuario.github.io/bitacora-restaurante/`
6. Abre esa URL desde tu celular o computadora.

## Cómo instalarla como app (PWA)

- **Android (Chrome):** abre la URL, te debería aparecer un botón "Instalar app" en la página, o desde el menú (⋮) → "Instalar aplicación".
- **iPhone (Safari):** abre la URL → toca el botón de compartir (cuadrado con flecha) → "Agregar a pantalla de inicio". iOS no muestra el botón de instalación automático, así que este paso es obligatorio ahí.
- **Computadora (Chrome/Edge):** abre la URL → aparece un ícono de instalación en la barra de direcciones, o usa el botón "Instalar app" que aparece abajo a la derecha.

## Importante sobre HTTPS

Las PWA (service workers) **solo funcionan bajo HTTPS** (o `localhost`). GitHub Pages ya da HTTPS automático, así que una vez publicada ahí, funcionará sin configurar nada extra.

## Cómo funciona la racha

- Cada día del plan se "abre" según la fecha real (Día 1 = el día que la abriste por primera vez).
- Tienes que presionar **"Cerrar día"** el mismo día para que cuente. Si completaste el 70% o más de las tareas, ganas puntos y suma racha. Si cierras con menos, pierdes puntos y la racha se reinicia.
- Si **no abres la app y no cierras el día**, al volver a abrirla se detecta el o los días perdidos, la racha se apaga y se restan puntos automáticamente.

## Cómo editar el plan de tareas

Si quieres cambiar las tareas de cada día, abre `index.html` y busca el bloque `const PLAN = [...]` cerca del inicio del `<script>`. Cada objeto `{ title: "...", tasks: [...] }` es un día.
