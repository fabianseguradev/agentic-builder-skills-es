# Stuck / Unstick

Claude te sigue dando lo que no es y estás dando vueltas en círculos. Esto te saca de ahí.

Hay cinco trampas en las que caen los principiantes, y cada una tiene una salida específica: el pedido era demasiado grande, estás describiendo el arreglo en lugar de lo que viste, el chat está contaminado después de 40 mensajes, cambiaste tres cosas a la vez, o estás intentando editar código a mano. Este skill nombra la trampa y **te da la oración exacta para enviar a continuación** — escrita para ti, lista para copiar.

## Instalación

1. Copia la carpeta `stuck-unstick` en tu directorio de skills de Claude Code:
   ```bash
   cp -r stuck-unstick ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/stuck-unstick`.

## Cómo usarlo

No necesita configuración. Escribe `/stuck-unstick` cuando estés atascado. Hace dos preguntas — qué pediste y qué recibiste en su lugar — y luego nombra en qué trampa estás y te escribe tu siguiente mensaje.

Obtienes el diagnóstico y la oración guardados en `~/build-log.md`, más permiso explícito para hacer `/rewind` y reiniciar limpio si dos intentos más no funcionan. Reiniciar una pieza de trabajo es barato. Pelear contra una dirección rota durante tres noches no lo es.
