# Deploy It

Toma lo que acabas de construir y ponlo en una dirección web pública real, gratis, en unos diez minutos.

Hasta que tenga un link, lo que hiciste no termina de contar — nadie puede abrirlo. Este skill te guía por el registro en Vercel un clic a la vez, explica el paso de GitHub en lenguaje simple en lugar de jerga y resuelve las tres cosas que de verdad se rompen para los principiantes. La idea de fondo es que **feo pero en línea le gana a bonito pero local**: la repetición que cuenta no es el pulido, es mandarle el link a una persona real.

## Instalación

1. Copia la carpeta `deploy-it` en tu directorio de skills de Claude Code:
   ```bash
   cp -r deploy-it ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/deploy-it`.

## Cómo usarlo

No necesita configuración. Primero construye algo con `/first-website`, `/landing-page`, `/link-in-bio`, `/sales-page` o `/simple-game`, y luego escribe `/deploy-it`.

Encuentra lo que construiste, prepara la parte de GitHub por ti y te da los pasos de Vercel uno a la vez — tú haces clic, él espera. Sin tarjeta, sin código, sin leer logs de errores. Si la página sale en blanco o el repo no aparece en la lista, ya conoce esos casos y los resuelve.

Terminas con un link `.vercel.app` en vivo, y se agrega a `~/my-links.md` para que vayas armando una lista de todo lo que has lanzado. Luego ábrelo en tu teléfono y mándale el link a una persona hoy.
