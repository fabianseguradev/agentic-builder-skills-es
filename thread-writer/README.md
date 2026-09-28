# Thread Writer

Convierte una idea en un hilo de X o un post largo de LinkedIn que la gente lee hasta el final.

Los hilos fallan en el medio, cuando una línea le da permiso al lector para dejar de leer. Este skill construye uno donde el gancho hace una promesa que de verdad cumple, un número o momento real aparece temprano para que la gente confíe en ti, y el único trabajo de cada línea es arrastrarlos hacia la siguiente. **Una idea por línea. Sin apilar.**

## Instalación

1. Copia la carpeta `thread-writer` en tu directorio de skills de Claude Code:
   ```bash
   cp -r thread-writer ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/thread-writer`.

## Cómo usarlo

Ejecuta `/personalize` una vez primero para que el skill escriba con tu voz. Luego escribe `/thread-writer` y describe la idea, más cualquier cosa real a la que puedas apuntar — un número que mediste, una noche en que algo se rompió, un antes y un después.

Comprime tu idea a una oración, escribe tres ganchos y elige uno, construye el cuerpo línea por línea y te da un final que aterriza en lugar de apagarse. Lo obtienes con el formato de X (posts numerados) o LinkedIn (un bloque), guardado en `~/threads/`.
