# Fable Goal Prompt Writer

Suelta tu idea en voz alta, tal como te salga, y recibe un prompt `/goal` excepcional que puedes pegar directamente en una sesión nueva de Fable.

Este skill no construye la cosa. Diseña el prompt que construye la cosa. La filosofía es simple: **quítate del camino del modelo.** Un gran prompt `/goal` clava *qué* quieres, le da al modelo sus herramientas, concede libertad creativa real sobre el *cómo* y exige que el modelo verifique su propio trabajo antes de dar algo por terminado.

## Instalación

1. Copia la carpeta `fable-goal` en tu directorio de skills de Claude Code:
   ```bash
   cp -r fable-goal ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/fable-goal`.

## Cómo usarlo

Escribe `/fable-goal` y luego describe lo que quieres, por desordenado que sea. El skill extrae el entregable, llena los huecos pequeños con valores razonables por defecto, hace una pregunta solo cuando la respuesta de verdad cambiaría el prompt y te entrega un prompt `/goal` terminado en un bloque listo para copiar, con una lista corta de los supuestos que asumió.

Pega ese prompt en una sesión nueva de Fable y déjalo trabajar.
