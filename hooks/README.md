# YouTube Hook Generator

Ganchos para tu video, construidos sobre el marco de Kallaway — cada uno puntuado, y los tres mejores entregados como un gancho visual, hablado y de texto que encajan entre sí.

La idea detrás: la gente hace clic por una de cuatro cosas — dinero, tiempo, salud o estatus. Pero si lo dices directamente, se les activa el detector de mentiras. Así que el skill apunta **a un paso de distancia del deseo**, a un sustituto que la gente sí cree. "Automatiza la parte de tu trabajo que odias" le gana a "gana más dinero".

## Instalación

1. Copia la carpeta `hooks` en tu directorio de skills de Claude Code:
   ```bash
   cp -r hooks ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/hooks`.

## Cómo usarlo

Lee tu perfil de marca en `~/.claude/brand-profile.md`, así que ejecuta `/personalize` primero si no lo has hecho. Así es como los ganchos suenan a tu audiencia en lugar de a texto genérico.

Escribe `/hooks` y el tema de tu video, el esquema o los puntos clave. Si solo das un tema, hace una pregunta: ¿qué es lo más sorprendente de este video? Recibes el deseo con el que lo relacionó, cinco variaciones de gancho, los tres mejores desarrollados por completo con sus puntajes y una recomendación directa de cuál usar.
