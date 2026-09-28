# Safety Net

Configura tus dos sistemas de deshacer para que puedas experimentar sin preocuparte por arruinar tu proyecto.

Los principiantes construyen con timidez porque creen que un mal prompt arruina todo. En realidad tienes dos deshacer distintos: `/rewind` para deshacer al instante el último movimiento, y puntos de control de Git para guardados permanentes a los que puedes volver días después. **Rewind deshace movimientos, los puntos de control guardan días.** Este skill configura ambos en el proyecto que tienes abierto ahora mismo, hace tu primer punto de control real y te deja una hoja de referencia de una página.

## Instalación

1. Copia la carpeta `safety-net` en tu directorio de skills de Claude Code:
   ```bash
   cp -r safety-net ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/safety-net`.

## Cómo usarlo

No necesita configuración. Escribe `/safety-net` y di en qué proyecto estás trabajando. Te hace probar `/rewind` una vez con un cambio descartable para que el miedo desaparezca, comprueba si el proyecto tiene Git y lo configura si no, y luego hace por ti tu primer punto de control con nombre. Nunca escribes un comando de Git — dices una oración, Claude la ejecuta.

Obtienes `~/claude-safety-net.md`: una hoja de referencia de una página con los guiones exactos de recuperación para "lo rompí", "vuelve un paso atrás" y "vuelve a esta mañana", más el movimiento para conservar ambas versiones cuando quieres recuperar la vieja pero no perder lo que hiciste desde entonces. Mantenla abierta en una pestaña mientras construyes.
