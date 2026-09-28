# Decision Helper

Estás atascado entre opciones. Esto te lleva a una decisión hoy, no a otra lista de pros y contras.

Estar atascado rara vez es por falta de información. Es una restricción sin nombre, o dos cosas que quieres y que no pueden ganar ambas. Así que este skill pone sobre la mesa las opciones que *no habías* enumerado, te hace decir qué estás optimizando de verdad, saca a la luz lo que no has admitido y luego **toma la decisión** — una recomendación, una razón, un primer paso.

## Instalación

1. Copia la carpeta `decision-helper` en tu directorio de skills de Claude Code:
   ```bash
   cp -r decision-helper ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/decision-helper`.

## Cómo usarlo

No necesita configuración. Escribe `/decision-helper` y describe en qué estás atascado, por desordenado que sea — "no puedo decidir si renunciar" basta para empezar.

Te pregunta cómo se ve ganar, busca la restricción que no has dicho en voz alta y luego comprueba qué tan difícil es deshacer la decisión. Si es barata de revertir, decides ahora y avanzas. Si es difícil de revertir, una verificación específica con fecha. Terminas con una recomendación, lo que te cuesta, lo que demostraría que está mal y una cosa para hacer hoy. Guardado en `~/decisions/`.
