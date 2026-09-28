# Session Wrap-Up

Termina tu sesión de construcción para que reabrirla mañana tome cinco minutos, no treinta.

Construyes durante 90 minutos, cierras la laptop y vuelves dos noches después sin idea de dónde estabas. La mitad de la siguiente sesión se va en recordar. Este skill son los últimos diez minutos de la noche: revisa qué cambió realmente, separa lo que funciona de lo que está a medias y escribe **una línea** que le dice al tú de mañana exactamente por dónde retomar. Una línea, no una lista de tareas — tres elementos significa que lees los tres y no empiezas ninguno.

## Instalación

1. Copia la carpeta `session-wrapup` en tu directorio de skills de Claude Code:
   ```bash
   cp -r session-wrapup ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/session-wrapup`.

## Cómo usarlo

No necesita configuración. Cuando termines de construir por la noche, escribe `/session-wrapup`. Revisa qué cambió en el proyecto en lugar de pedirte que lo recuerdes, te dice claramente qué funciona y qué está a medio terminar, y te propone guardar un punto de control antes de cerrar.

Agrega una entrada con fecha a `~/build-log.md`. Mañana, abre ese archivo primero, lee la última entrada, haz el primer paso y nada más.
