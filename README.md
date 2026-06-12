# Portfolios Cursos

Esta web muestra una lista de cursos y sus proyectos asociados usando archivos JSON como fuente de datos.

## Estructura del proyecto

- `index.html`: Página principal que carga `data/courses.json` y muestra los cursos como tarjetas.
- `data/courses.json`: Define cada curso con campos como `id`, `name`, `dataFile`, `startDate` y `description`.
- `data/curso-*.json`: Archivos específicos de cada curso que contienen la lista de proyectos.
- `pages/curso.html`: Página dinámica que usa el parámetro `?id=` para cargar los datos del curso seleccionado y mostrar sus proyectos.

## Cómo funciona

1. `index.html` hace `fetch` de `data/courses.json`.
2. Para cada curso crea una tarjeta con un enlace a `pages/curso.html?id=<curso>`.
3. `pages/curso.html` lee `id` de la URL, carga `data/courses.json` para obtener el curso y luego carga el archivo JSON asociado en `dataFile`.
4. Muestra el nombre del curso, la descripción, la fecha de inicio y los proyectos vinculados.

## Despliegue en Netlify

1. Crea una cuenta gratuita en [Netlify](https://www.netlify.com/).
2. Conecta tu repositorio GitHub:
   - Selecciona `New site from Git`.
   - Escoge `GitHub` como proveedor.
   - Autoriza el acceso a `albertomozo/portfolios-cursos`.
3. Configura el sitio:
   - Branch: `main`.
   - Build command: deja vacío (no hay compilación).
   - Publish directory: `/`.
4. Haz deploy.

Netlify publicará la web estática en una URL como `https://portfolio-cursos.netlify.app`.

## URLs importantes

- Sitio: https://portfolio-cursos.netlify.app
- GitHub: https://github.com/albertomozo/portfolios-cursos

## Notas adicionales

- Esta web es completamente estática y funciona en cualquier hosting de archivos estáticos.
- Si deseas cambiar cursos o proyectos, solo actualiza los archivos JSON en `data/`.
- La página dinámica `pages/curso.html` permite añadir cursos nuevos sin crear nuevas páginas HTML.
