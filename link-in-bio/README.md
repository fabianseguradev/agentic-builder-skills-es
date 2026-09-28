# Link in Bio

Tu propia página de links con tu marca — foto, nombre, pitch de una línea y 4-6 botones — construida en una noche y mejor que el Linktree que tienen todos los demás.

El verdadero skill aquí no es el diseño, es **el orden de los links**. La gente toca uno de los dos primeros botones y se va, así que lo que te hace ganar dinero va arriba y todo lo que está por debajo del botón cuatro es casi invisible. El skill ordena tus links frente a ti, recorta la lista y reescribe cada etiqueta de botón como una acción simple.

## Instalación

1. Copia la carpeta `link-in-bio` en tu directorio de skills de Claude Code:
   ```bash
   cp -r link-in-bio ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/link-in-bio`.

## Cómo usarlo

Ejecuta `/personalize` primero para que la página suene y se vea como tú. Luego escribe `/link-in-bio` y vuelca todos los links que querrías tener ahí.

Te pide una foto, tu nombre y un pitch de una línea, luego ordena y recorta tus links y explica cada posición. Construye un solo `index.html` autocontenido diseñado primero para el teléfono, porque ahí es donde casi todo el mundo lo abre. Previsualízalo a ancho de teléfono, haz la prueba del pulgar con los botones y reacciona con palabras simples. Obtienes un archivo en `~/sites/<your-project>/index.html` — ejecuta `/deploy-it` para convertirlo en un link real para tu bio.
