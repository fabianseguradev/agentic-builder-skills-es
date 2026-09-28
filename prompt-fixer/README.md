# Prompt Fixer

Pega el prompt que te dio un mal resultado. Recibe por qué falló y el prompt reescrito para ejecutar en su lugar.

Cuando el resultado está mal, los principiantes culpan al modelo. Casi siempre es **un prompt flaco, no un mal modelo.** Este skill revisa siete causas habituales — demasiado vago, tres pedidos en uno, sin restricciones, sin formato, sin listo-cuando, falta de contexto que Claude no podía saber y pedir código en lugar de un resultado — nombra la que hizo más daño y te entrega una versión arreglada que puedes ejecutar ahora mismo.

## Instalación

1. Copia la carpeta `prompt-fixer` en tu directorio de skills de Claude Code:
   ```bash
   cp -r prompt-fixer ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/prompt-fixer`.

## Cómo usarlo

No necesita configuración. Escribe `/prompt-fixer` y pega el prompt que usaste. Si todavía tienes lo que devolvió, pégalo también — hace el diagnóstico más preciso. Luego di en una oración lo que realmente querías.

Recibes la causa en lenguaje simple, el prompt reescrito en un bloque listo para copiar y una nota corta sobre qué cambió y por qué. Se guarda en `~/briefs/fixed-<name>.md`. Ejecuta el prompt arreglado en una sesión **nueva** — reutilizar la conversación vieja arrastra con ella la respuesta equivocada.
