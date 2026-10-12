# NutriDía v5

Aplicación web progresiva para registro nutricional diario.

## Publicar
Sube `index.html`, `manifest.webmanifest`, `sw.js` e `icon.svg` a la raíz del repositorio de GitHub Pages y confirma los cambios. El service worker usa la caché `nutridia-shell-v5` para forzar la renovación de los recursos de interfaz.

## Privacidad
Perfil, objetivos, tema, catálogo consultado y registro diario se guardan en `localStorage` del navegador/dispositivo. No se envían al repositorio de GitHub Pages. Las consultas de productos sí se envían a las APIs externas configuradas en la app. Borrar datos de Safari puede eliminar registros; usar copia de seguridad antes de cambiar de dispositivo.

## Estimaciones
El gasto energético es una estimación orientativa basada en Mifflin–St Jeor y factores de actividad seleccionados por el usuario. No constituye consejo médico ni garantiza un peso futuro. Revisar la evolución real y consultar a profesionales en caso de necesidades clínicas.
