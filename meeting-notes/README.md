# Meeting Notes

Pega la transcripción de una reunión y recibe un resumen limpio en markdown con cada tarea asignada a una persona.

La mayoría de las herramientas de notas te entregan un muro de texto que nunca vuelves a leer. Esta extrae solo lo que necesitaría alguien que se perdió la llamada: qué se decidió, quién debe qué y qué sigue abierto. La regla que la mantiene útil: **las decisiones y las tareas no son lo mismo.** Las decisiones son resultados. Las tareas son cosas por hacer con el nombre de un responsable.

## Instalación

1. Copia la carpeta `meeting-notes` en tu directorio de skills de Claude Code:
   ```bash
   cp -r meeting-notes ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/meeting-notes`.

## Cómo usarlo

Escribe `/meeting-notes` y pega tu transcripción. Funciona con lo que genere cualquier herramienta — Fireflies, Otter, Granola, Zoom. Recibes un archivo en `~/meeting-notes/` nombrado por fecha y tema, con un resumen corto, las decisiones, las tareas agrupadas por persona, las preguntas abiertas y los próximos pasos. Todo lo que no puede asignar con seguridad queda marcado para que lo corrijas en lugar de confiar en una suposición.

No necesita configuración. Instálalo y pega.
