# LAS SEÑALES ESTÁN AQUÍ — aplicación Android

Primera base del proyecto Android. La aplicación abre el catálogo local dentro de un WebView, conserva los registros del navegador local y permite enlazar con fuentes online.

## Qué incluye esta primera base

- Interfaz en español con estética oscura y sello del proyecto.
- Catálogo inicial de casos, filtros y formulario para agregar registros.
- Sección de archivos oficiales/desclasificados con enlaces a fuentes originales.
- Videoteca minimalista: carátula provisional, título y año, sin tráileres ni sinopsis.
- Almacenamiento local de casos, exportación JSON a Descargas en Android y selector de archivos para importar copias.
- Acción de impresión del catálogo desde el menú de impresión de Android.
- Flujo de GitHub Actions para compilar un APK de depuración.

## Limitaciones conocidas

- El APK aún no está firmado para distribución pública.
- La sincronización automática entre dispositivos no está implementada.
- Los archivos oficiales y enlaces externos necesitan Internet; los registros guardados se conservan localmente.
- Las carátulas de la videoteca son provisionales. Se podrán sustituir por imágenes con fuentes y permisos adecuados.
- La base de datos inicial es pequeña y contiene ejemplos que requieren ampliación y verificación documental.

## Compilar en GitHub desde una computadora

1. Crea un repositorio nuevo en GitHub llamado `las-senales-estan-aqui`.
2. Sube el contenido de esta carpeta a la rama `main` (no subas la carpeta contenedora como una carpeta anidada; sube los archivos y carpetas que contiene).
3. En GitHub, abre **Actions** y habilita los flujos de trabajo si GitHub lo solicita.
4. El flujo **Construir APK Android** se ejecutará al subir código o puedes iniciarlo con **Run workflow**.
5. Al terminar, abre la ejecución correcta y descarga el artefacto `Las-Senales-Estan-Aqui-debug-apk`.
6. Descomprime el artefacto y copia `app-debug.apk` al teléfono Android para instalarlo.

## Desarrollo local

Requiere Android SDK y Java 17. Con Gradle 8.9 instalado, ejecuta:

```bash
gradle assembleDebug
```

El APK se genera en `app/build/outputs/apk/debug/app-debug.apk`.
