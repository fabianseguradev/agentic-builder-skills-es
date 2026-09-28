# Quote Calculator

Construye un pequeño widget de cotización instantánea para un negocio de servicios — el comprador elige algunas opciones, ve un rango de precio en segundos y deja sus datos.

Los negocios de servicios pierden leads en el "llame para cotizar". La gente quiere un número aproximado antes de levantar el teléfono. Esto construye la herramienta que se lo da, en un solo archivo HTML autocontenido, sin backend y sin nada que pagar. Dos reglas lo rigen todo: **muestra siempre un rango, nunca un único número fijo**, y captura siempre el lead después del rango, nunca antes.

## Instalación

1. Copia la carpeta `quote-calculator` en tu directorio de skills de Claude Code:
   ```bash
   cp -r quote-calculator ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/quote-calculator`.

## Cómo usarlo

No necesita configuración. Escribe `/quote-calculator` y describe el negocio — mudanzas, limpieza, jardinería, pintores, retiro de escombros, lavado a detalle. Te guía por la lógica real de precios: la base, las tres a cinco cosas que mueven el número, y el piso y el techo.

Obtienes una página que funciona en `~/sites/<business>-quote/index.html` más un archivo de notas de precios, probada contra tres trabajos reales anteriores. También sirve como primer trabajo pagado: construye una para un negocio local usando sus precios reales y mándales el link.
