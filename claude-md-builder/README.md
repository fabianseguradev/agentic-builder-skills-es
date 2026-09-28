# CLAUDE.md Builder

Deja de volver a explicar tu proyecto cada vez que abres Claude Code.

Claude empieza cada sesión en blanco. Un archivo `CLAUDE.md` en la carpeta de tu proyecto se lee automáticamente al inicio de cada sesión, así que tus reglas se mantienen. El truco que la mayoría hace mal: **lo corto le gana a lo completo.** Es un centro de mando, no una autobiografía — un archivo de memoria inflado entierra las reglas que realmente importan.

## Instalación

1. Copia la carpeta `claude-md-builder` en tu directorio de skills de Claude Code:
   ```bash
   cp -r claude-md-builder ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/claude-md-builder`.

## Cómo usarlo

No necesita configuración. Abre Claude Code dentro de la carpeta de tu proyecto y escribe `/claude-md-builder`. Te hace seis preguntas — qué es el proyecto, lo único que tiene que hacer, tus reglas de siempre, tus reglas de nunca, dónde viven los archivos y cómo quieres que te hablen. Luego recorta tus respuestas a menos de 40 líneas y escribe `CLAUDE.md` en esa carpeta.

Al final te dice cómo demostrar que funcionó: empieza una sesión nueva y pregunta "¿cuáles son mis reglas?". Si Claude responde sin que expliques nada, la memoria está activa.
