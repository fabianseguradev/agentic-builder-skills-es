# Launch Plan

Un plan día por día para lanzar lo que construiste, dimensionado a la audiencia que realmente tienes.

Un lanzamiento es un pico, no tu motor. Toma el interés que ya construiste y lo concentra en unos pocos días para que las ventas lleguen juntas. Este skill elige el tipo de lanzamiento que encaja con tu etapa (preventa, lista de espera, directorio u oferta por tiempo limitado), fija una fecha real y un número real, y te dice qué hacer cada día. Si tu audiencia todavía es básicamente ninguna, te lo dice en lugar de prometerte un pico que no puede pasar.

## Instalación

1. Copia la carpeta `launch-plan` en tu directorio de skills de Claude Code:
   ```bash
   cp -r launch-plan ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/launch-plan`.

## Cómo usarlo

Ejecuta `/personalize` una vez primero para que conozca tu oferta, tu audiencia y tu voz. Luego escribe `/launch-plan` y dile qué estás lanzando.

Te hace cinco preguntas, incluida qué tan grande es realmente tu audiencia, y luego recomienda un tipo de lanzamiento y explica por qué ese. Recibes un plan guardado en `~/launches/launch-<your-offer>-<date>.md` con el tipo de lanzamiento, la fecha, el número al que apuntas, una lista de lo que todavía te falta hacer y un cronograma con fechas desde el primer adelanto hasta el día de cierre. También te ofrecerá redactar los mensajes con tu voz.
