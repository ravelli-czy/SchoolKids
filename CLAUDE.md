# Instrucciones para Claude

Este repo es un sitio estático de un solo archivo (`index.html`). No hay build, framework ni dependencias.

## Tarea: publicar en GitHub + Vercel
1. `git init`, rama `main`, commit inicial con todos los archivos.
2. Crear el repo en GitHub con `gh repo create eye-detective --public --source . --push`
   (si el usuario prefiere privado, usar `--private`). Si `gh` no está autenticado, pedirle al usuario que corra `gh auth login`.
3. Deploy en Vercel:
   - Opción A (CLI): `npx vercel --prod`. Al configurar: proyecto nuevo `eye-detective`, directorio `./`, framework "Other", sin build command, output directory por defecto. Si no está logueado, pedir `npx vercel login`.
   - Opción B (dashboard): importar el repo desde vercel.com/new con preset "Other". Esto deja deploy automático en cada push a `main`.
4. Entregar al usuario la URL de producción (`https://eye-detective*.vercel.app`).

## Reglas
- No modificar `index.html` salvo que el usuario lo pida.
- No agregar frameworks ni pasos de build.
- Para cambios futuros: editar `index.html`, commit y push; Vercel redeploya solo si el repo está conectado.
