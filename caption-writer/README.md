# Caption Writer

Convierte algo que construiste en un caption que puedes pegar y publicar, con tu propia voz.

La mayoría de la gente termina algo y luego no dice nada, porque publicar se siente como presumir. Este skill lo resuelve eligiendo una de cuatro formas de post que funcionan de forma confiable — mostrar la cosa, la lección de un error, el antes/después o la actualización honesta de progreso — y escribiendo una primera línea que hace todo el trabajo. **Muestra la cosa, no te anuncies a ti mismo.**

## Instalación

1. Copia la carpeta `caption-writer` en tu directorio de skills de Claude Code:
   ```bash
   cp -r caption-writer ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/caption-writer`.

## Cómo usarlo

Ejecuta `/personalize` una vez primero para que el skill conozca tu voz y tu audiencia. Luego escribe `/caption-writer` y describe lo que hiciste, por desordenado que sea — un link, una captura de pantalla o simplemente "construí esta cosa que hace X".

Te pregunta en qué plataforma vas a publicar, elige la forma del post, escribe tres primeras líneas y te dice cuál usaría, y luego te entrega el caption terminado con el tamaño adecuado para Instagram, LinkedIn, X o TikTok. Si hay un link, termina con una palabra clave para comentarios en lugar de una URL directa, porque los comentarios se convierten en conversaciones. El caption se guarda en `~/captions/`.
