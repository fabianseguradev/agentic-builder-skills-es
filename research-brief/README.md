# Research Brief

Convierte "necesito entender X antes del lunes" en una página con la que de verdad puedes entrar a una sala.

No una lista de lecturas ni veinte pestañas abiertas. La respuesta va en las primeras tres líneas, y luego el brief clasifica todo en **lo que está establecido, lo que se discute y lo que nadie sabe todavía** — con cada número llevando la fecha de la que salió, y todo lo que no se pudo comprobar marcado como no verificado en lugar de adivinado.

## Instalación

1. Copia la carpeta `research-brief` en tu directorio de skills de Claude Code:
   ```bash
   cp -r research-brief ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/research-brief`.

## Cómo usarlo

No necesita configuración. Escribe `/research-brief` y di qué necesitas entender — "ponme al día sobre la semana de cuatro días, tengo una llamada el lunes".

Hace una pregunta: qué vas a hacer con esto. Un brief para una compra se ve distinto a uno para una reunión. Luego busca en la web donde puede, va a las fuentes primarias en lugar de a artículos sobre ellas, y busca deliberadamente el caso más fuerte en contra. Obtienes una página con fuentes guardada en `~/research/`, que termina con una lista honesta de lo que no pudo confirmar.
