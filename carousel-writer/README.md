# Carousel Writer

Consigue las palabras exactas para cada slide de un carrusel, más una nota de qué va en cada slide, listo para armar en Canva o entregárselo a Claude.

Los carruseles se guardan y se comparten más que cualquier otro post, y la mayoría de la gente los mata en el slide uno escribiendo un párrafo. Este skill escribe slide por slide con la menor cantidad posible de palabras y trata el slide 1 como un trabajo aparte — porque **es el único slide que la mayoría de la gente llegará a ver.** Escribe las palabras, no las imágenes.

## Instalación

1. Copia la carpeta `carousel-writer` en tu directorio de skills de Claude Code:
   ```bash
   cp -r carousel-writer ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/carousel-writer`.

## Cómo usarlo

Ejecuta `/personalize` una vez primero para que los slides suenen como tú. Luego escribe `/carousel-writer` y di de qué trata el carrusel y qué debería poder hacer alguien después de deslizarlo.

Obtienes de 7 a 10 slides, cada uno con un titular corto, una línea de apoyo opcional y una línea que describe qué va en el slide. El slide 1 viene con tres opciones. El último slide es el pedido. También te entrega un prompt listo para copiar para construir todo como una página web en una sesión nueva de Claude Code. Todo se guarda en `~/carousels/`.
