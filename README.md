# NutriDía v10 — versión final para publicar

## Qué cambia
- Solo cuatro pestañas: Balance diario, Comidas, Historial y Mi perfil.
- Paletas pastel suaves; la elección de color está dentro de Mi perfil.
- Se elimina por completo la tarjeta «Mis objetivos diarios». La única meta visible en Balance es la meta energética calculada desde Mi perfil, al final del balance.
- Comidas muestra primero los alimentos registrados y debajo el buscador.
- Historial incorpora calendario con ✓ dentro del rango, ✕ fuera del rango y ○ pendiente; el listado explica por qué un día cerrado queda fuera del rango.
- Perfil, diario, catálogo, preferencias y cierres se guardan en localStorage del mismo origen de GitHub Pages. «Guardar copia de seguridad» descarga un JSON completo y «Recuperar perfil y datos» lo importa.
- Se conserva el nombre de las claves locales anteriores para preservar registros de versiones previas. El service worker se versiona para actualizar la caché.
- Se evita la descarga automática masiva de catálogo al abrir. La búsqueda online consulta MercaAPI y Open Food Facts; los resultados consultados se guardan localmente. «Actualizar base de datos» refresca solo una muestra local acotada para evitar saturar el almacenamiento del iPhone.

## Publicación
Sube a la raíz del repositorio existente los cuatro archivos: `index.html`, `manifest.webmanifest`, `sw.js` e `icon.svg`, y confirma el commit. GitHub Pages reutilizará la URL actual.

## Datos y privacidad
La información personal se guarda en el almacenamiento del navegador para ese dominio/dispositivo y no se sube a GitHub. Si borras los datos del sitio, cambias de navegador o dispositivo, puede hacer falta restaurar la copia JSON. Conviene guardar periódicamente esa copia en Archivos/iCloud Drive. Las búsquedas nutricionales consultan fuentes externas y envían el texto buscado. MercaAPI no es oficial y Open Food Facts es colaborativa; comprobar etiquetas para datos críticos.


## v11
- Corrige el calendario mensual en móvil con una cuadrícula de siete columnas y controles de mes centrados.
- Amplía la selección de temas hasta 15 tonos pastel.

### v12 (versión profesional)
- Barra de navegación inferior con iconos en móvil (estilo app nativa) y control segmentado en escritorio.
- Logo vectorial integrado en la cabecera y fecha del día visible.
- Iconos PNG para la pantalla de inicio del iPhone (apple-touch-icon) y Android, más icono «maskable».
- Campos a 16 px en móvil para evitar el zoom automático de Safari.
- Corrección de contrastes (barra de calorías, textos en tono pastel ilegibles).
- Tarjetas, botones, foco y estados hover/pulsado unificados.
- Se mantienen las mismas claves de almacenamiento: no se pierde ningún dato.

Archivos a subir a la raíz: index.html, manifest.webmanifest, sw.js, icon.svg, icon-maskable.svg, apple-touch-icon.png, icon-192.png, icon-512.png.
