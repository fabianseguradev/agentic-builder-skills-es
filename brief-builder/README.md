# Brief Builder

Describe lo que quieres con tus propias palabras desordenadas y recibe un prompt lo bastante afilado como para pegarlo directo en Claude.

La mayoría de los malos resultados vienen de un pedido flaco. Este skill completa las cinco partes que un prompt necesita para funcionar — **CONTEXTO, OBJETIVO, RESTRICCIONES, FORMATO, LISTO-CUANDO** — y te muestra el antes y el después para que veas exactamente qué marcó la diferencia. También te da una versión comprimida de una sola oración para los cuarenta pedidos pequeños que haces cada semana.

## Instalación

1. Copia la carpeta `brief-builder` en tu directorio de skills de Claude Code:
   ```bash
   cp -r brief-builder ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/brief-builder`.

## Cómo usarlo

No necesita configuración. Escribe `/brief-builder` y describe lo que quieres construir, por vago que sea. Te devuelve el entregable para confirmarlo, pregunta solo por los detalles que realmente cambiarían la respuesta y completa los huecos con supuestos claramente marcados en lugar de interrogarte.

Obtienes un brief listo para copiar guardado en `~/briefs/`, más la versión comprimida de una línea: "Dado [contexto], haz [objetivo], sin [restricción], con formato de [formato] — listo cuando [listo-cuando]." Pega la versión larga en una sesión nueva de Claude. Si el resultado no es el correcto, cambia una parte del brief y ejecútalo de nuevo.
