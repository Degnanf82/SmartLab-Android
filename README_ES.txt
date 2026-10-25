PROYECTO ANDROID SMARTLAB — v0.1.1

Incluye:
- Proyecto fuente Android con interfaz demo.
- Workflow de GitHub Actions para compilar una APK de depuración en la nube.

CÓMO COMPILAR DESDE EL MÓVIL:
1. Entra en https://github.com/ e inicia sesión o crea una cuenta.
2. Crea un repositorio nuevo llamado SmartLab-Android. Para este prototipo, un repositorio privado es razonable.
3. Sube el CONTENIDO de esta carpeta al repositorio, conservando las rutas y la carpeta oculta .github/workflows/build.yml.
   Consejo: al subir desde el navegador móvil, comprueba que se sube la carpeta .github; si la interfaz no permite subir carpetas, usa el editor web o GitHub Codespaces.
4. Abre la pestaña Actions del repositorio.
5. Selecciona “Build SmartLab Android APK” y pulsa “Run workflow” si no se ha iniciado automáticamente.
6. Espera a que el trabajo termine en verde.
7. Abre la ejecución terminada y descarga el artefacto “SmartLab-debug-APK”.
8. Extrae el ZIP descargado; dentro estará app-debug.apk. Ábrelo en Android y, si te lo solicita, permite instalar apps desde esa fuente.

El workflow utiliza GitHub Actions para ejecutar Gradle 8.9 con Java 17 y generar app/build/outputs/apk/debug/app-debug.apk.

LIMITACIONES:
- Este es un APK de depuración, no una versión de publicación firmada con una clave privada propia.
- La interfaz usa datos simulados. No conecta todavía con hardware SmartLab por Wi-Fi ni USB-C.
- No uses las lecturas demo para tomar decisiones eléctricas.
- No publiques secretos, contraseñas ni claves de firma en el repositorio.
