# NutriDía · Calculadora nutricional

Aplicación web móvil para registrar alimentos, calcular calorías/macros y seguir objetivos.

## Datos locales y recuperación

El perfil, los objetivos, el diario, los cierres de día, el tema, los alimentos personalizados y el catálogo consultado se guardan automáticamente en el almacenamiento local del navegador. Al volver a abrir la misma URL en el mismo navegador, se vuelven a cargar.

Esto no es sincronización en la nube: borrar los datos del sitio, usar otro navegador/dispositivo o algunas operaciones de privacidad pueden eliminar los datos locales. En Mi perfil, usa **Guardar copia de seguridad** y guarda el JSON en Archivos/iCloud Drive. Para recuperar, abre NutriDía y usa **Recuperar perfil y datos** para importar esa copia. La restauración sustituye los datos actuales por los de la copia.

## Publicación

Sube `index.html`, `manifest.webmanifest`, `sw.js` e `icon.svg` a la raíz de un repositorio GitHub Pages y activa Pages desde la rama `main` y carpeta `/root`.

## Catálogo

El catálogo se consulta en fuentes externas no oficiales/colaborativas. La disponibilidad y la cobertura pueden cambiar.
