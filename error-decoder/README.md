# Error Decoder

Pega el texto en rojo. Recibe qué se rompió en lenguaje simple y la oración exacta que tienes que pegarle a Claude para arreglarlo.

El texto en rojo paraliza a los principiantes, y mucho de eso ni siquiera necesita arreglo. Este skill clasifica cada error en una de cuatro categorías — **Ruido, Cosmético, Bloqueado o Rebobínalo** — lo traduce a palabras de sobremesa y te entrega una oración lista para copiar y enviarle de vuelta a Claude. Nunca abres un archivo ni editas una línea de código.

## Instalación

1. Copia la carpeta `error-decoder` en tu directorio de skills de Claude Code:
   ```bash
   cp -r error-decoder ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/error-decoder`.

## Cómo usarlo

No necesita configuración. Escribe `/error-decoder` y pega lo que te asustó — un error, un muro de texto rojo, un mensaje que no entiendes. Te pregunta dos cosas: qué le acababas de pedir a Claude y si la cosa todavía funciona.

Recibes qué tan grave es, qué se rompió y por qué, lo que definitivamente NO le hizo a tus archivos y la oración para arreglarlo que tienes que pegar. Se guarda en `~/claude-errors/` con la fecha, así que la carpeta se va convirtiendo en tu propio registro de solución de problemas. Si las cosas se enredan, te dice que uses `/rewind` en lugar de depurar — deshacer es más rápido que desenredar.
