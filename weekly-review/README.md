# Weekly Review

Un reinicio dominical de 20 minutos que te muestra qué lanzaste de verdad y elige la única cosa para la próxima semana.

El progreso de cada noche es invisible. Construyes en horas robadas, algunas noches no llegan a nada, y para el domingo se siente como si no hubieras hecho nada — que es la razón principal por la que la gente abandona en el segundo mes. **El progreso es semanal, no nocturno.** Este skill lee tu registro de construcción para conseguir la evidencia real, saca una razón específica para todo lo que se estancó, y luego fuerza un recorte: nombras EL ÚNICO resultado para la próxima semana, y dices en voz alta qué estás dejando de lado.

## Instalación

1. Copia la carpeta `weekly-review` en tu directorio de skills de Claude Code:
   ```bash
   cp -r weekly-review ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/weekly-review`.

## Cómo usarlo

No necesita configuración. El domingo, escribe `/weekly-review`. Lee `~/build-log.md` y tus archivos de plan para que no tengas que recordar la semana, enumera qué se lanzó, indaga en por qué se estancó lo que se estancó y te hace elegir una cosa y estacionar el resto.

Obtienes `~/weekly-review.md` con los logros de la semana, la única cosa, dos elementos estacionados y tres movimientos específicos colocados en las noches que realmente tienes. Pon esos tres en tu calendario antes de cerrar la laptop.
