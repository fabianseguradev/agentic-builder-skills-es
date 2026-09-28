# Design Taste

Nombra 1-3 sitios que te encanten y recibe un sistema de diseño escrito al que puedes apuntar cada proyecto futuro.

El buen gusto no es un don, es un conjunto de decisiones que alguien dejó por escrito. Este skill extrae las decisiones reales de sitios que ya te gustan — códigos hex, combinación de fuentes, saltos de tamaño, pasos de espaciado — y las guarda en un archivo. **Decide una vez y deja de volver a decidir.** Cada proyecto después de esto lee ese archivo, así que tus páginas empiezan a verse como si vinieran de la misma persona.

## Instalación

1. Copia la carpeta `design-taste` en tu directorio de skills de Claude Code:
   ```bash
   cp -r design-taste ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/design-taste`.

## Cómo usarlo

No necesita configuración. Escribe `/design-taste` y nombra o pega 1-3 sitios cuyo aspecto te guste, más una oración sobre cómo quieres que se sienta la gente. Si no puedes nombrar ninguno, te da seis direcciones para elegir.

Recibes dos archivos: `~/.claude/design.md` con la paleta, las fuentes, la escala, el espaciado y una lista de lo que no se hace, y una página de vista previa que abres en tu navegador para verlo de verdad. Después de eso, empieza cualquier prompt de construcción con "Lee ~/.claude/design.md y síguelo."
