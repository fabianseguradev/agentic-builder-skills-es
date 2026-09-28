# Plan First

Consigue un plan escrito que apruebas antes de que Claude toque un solo archivo.

Construir demasiado grande es lo número uno que mata un proyecto de principiante. Describes el sueño completo, la construcción empieza sobre el sueño completo y cuatro noches después nada funciona. Este skill hace lo contrario: encuentra el **único trabajo** que tu proyecto tiene que hacer, pasa todo lo demás a una lista de "más adelante" y pone los pasos en un orden que de verdad puedes terminar en tus horas robadas.

## Instalación

1. Copia la carpeta `plan-first` en tu directorio de skills de Claude Code:
   ```bash
   cp -r plan-first ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/plan-first`.

## Cómo usarlo

No necesita configuración. Escribe `/plan-first` y describe lo que quieres construir, por grande y desordenado que sea. Te devuelve la idea, te hace nombrar el único trabajo y luego recorta fuerte — vas a ver exactamente qué va en la v1, qué queda esperando y por qué se hizo cada recorte.

Obtienes un archivo en `~/plans/<project>-plan.md` con el alcance de tu v1, tu lista de más adelante, los pasos en orden, una definición de terminado comprobable y un primer paso lo bastante pequeño como para empezar esta noche. No se construye nada hasta que digas que sí.
