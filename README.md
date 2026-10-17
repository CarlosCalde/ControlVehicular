# Mi Control Vehicular

PWA de mantenimiento vehicular sin dependencias, lista para Android, iPhone y GitHub Pages.

## Funciones
- Varios vehículos, kilometraje e intervalo personalizable (5.000 km por defecto).
- Aviso visual cuando faltan hasta 500 km y cuando el cambio está vencido.
- Historial de mantenimientos, taller, repuestos, fecha, costo y kilómetros.
- Exportación de respaldo JSON y CSV para Excel; restauración de JSON.
- Guardado local en el dispositivo, sin cuenta ni servidor.

## Publicación en GitHub Pages
1. Crea un repositorio público, por ejemplo `mi-control-vehicular`.
2. Sube **el contenido de esta carpeta** a la raíz del repositorio (no solo el ZIP).
3. Ve a **Settings → Pages → Build and deployment**, elige **Deploy from a branch**, `main`, `/ (root)`, y pulsa **Save**.
4. Cuando se publique, abre `https://TU-USUARIO.github.io/mi-control-vehicular/` desde el teléfono con internet.
5. iPhone: Safari → Compartir → **Añadir a pantalla de inicio** → Añadir. Android: Chrome → menú → **Instalar aplicación** o **Añadir a pantalla principal**.
6. Abre una vez la aplicación y luego podrás usarla sin internet.

## Advertencias importantes
- Los datos están **solo en el almacenamiento del navegador/PWA en ese dispositivo**. GitHub almacena el código, no los historiales. No se sincronizan entre teléfonos. Para transferirlos, exporta un JSON e impórtalo en el otro teléfono.
- El borrado de datos de navegación, eliminar la app o cambios en almacenamiento pueden borrar los registros. Exporta respaldos frecuentes.
- Los recordatorios son visuales al abrir la app, no notificaciones en segundo plano.
- La primera carga/instalación requiere internet y HTTPS (GitHub Pages proporciona HTTPS).
- El control de kilómetros es manual; no lee el odómetro del vehículo.
- Para desarrollo local utiliza un servidor HTTP (por ejemplo `python -m http.server 8000`), no `file://`.

## Novedades v2

- Lista de tareas habituales agrupadas en 7 categorías. Permite marcar varias tareas en un mismo servicio.
- Apartado independiente **Trabajo distinto / reparación** para trabajos personalizados.
- Las tareas seleccionadas se guardan en el historial y se exportan a CSV.
- Los registros existentes de la primera versión se conservan en el almacenamiento del mismo navegador al actualizar.
- El cambio de aceite marcado en una lista reinicia el próximo aviso del servicio de aceite. Los demás mantenimientos se registran sin periodicidad automática por ahora.
- Para actualizar GitHub Pages, sustituye los archivos del repositorio por los de esta versión; no es necesario crear otro repositorio.

## Versión 3: registro por tipo de trabajo
En **Historial → Registrar trabajo** se escoge **Mantenimiento** (preventivo) o **Correctivo** (reparación de fallas). Cada categoría presenta un catálogo diferente con casillas de selección múltiple. Se pueden añadir tareas no listadas y guardar todo como un solo registro con fecha, km, costo, taller y notas. Los trabajos anteriores se mantienen almacenados con la misma clave local. Antes de actualizar, exporta un respaldo desde la app.
