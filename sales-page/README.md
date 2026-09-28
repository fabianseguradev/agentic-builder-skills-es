# Sales Page

Una página que parece un producto real y que de verdad lo vende — construida en el orden que hace que la gente compre, no en el orden en que se te ocurra escribirlo.

La mayoría de las primeras páginas de ventas fallan por la secuencia. Abren con el producto, nombran el precio antes de que nadie quiera el resultado y entierran la prueba al final. Esta sigue problema → estado posterior → qué es → qué incluye → prueba → precio → garantía → preguntas frecuentes, con **un botón repetido tres veces** y el precio dicho exactamente una vez. La regla de fondo en todo: nunca pongas el precio antes del valor.

## Instalación

1. Copia la carpeta `sales-page` en tu directorio de skills de Claude Code:
   ```bash
   cp -r sales-page ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/sales-page`.

## Cómo usarlo

Ejecuta `/personalize` primero para que la página suene a ti. Luego escribe `/sales-page` y describe qué estás vendiendo.

Primero comprueba que tengas un precio real y una oferta real — si no, te manda a `/pricing-calculator` o `/offer-builder` y espera. Luego pregunta sobre el problema que siente la gente, qué incluye, qué prueba tienes de verdad y las tres razones por las que alguien diría que no. Escribe el texto, construye un solo `index.html` autocontenido y te hace leerlo en voz alta para detectar la vergüenza ajena.

Obtienes un archivo en `~/sites/<your-project>/index.html`. Ejecuta `/deploy-it` para publicarlo, y luego mándale el link a tres personas que ya te dijeron que estaban interesadas.
