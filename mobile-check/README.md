# Mobile Check

Mira la página que construiste tal como la ve una persona real en un teléfono, y recibe una lista numerada de arreglos que puedes pegarle directamente a Claude.

Construyes en una laptop. La mayoría de tus visitantes están en un teléfono, con una mano, medio distraídos. Esto revisa las siete cosas que realmente se rompen a 375 píxeles de ancho — scroll lateral, botones demasiado pequeños para tocar, texto diminuto, imágenes que desarman el diseño, un botón principal al que nadie llega y si la página se sigue leyendo con JavaScript desactivado. **Cada problema viene con la oración exacta para pegar de vuelta**, porque el movimiento de principiante es describir el síntoma, no editar el código.

## Instalación

1. Copia la carpeta `mobile-check` en tu directorio de skills de Claude Code:
   ```bash
   cp -r mobile-check ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/mobile-check`.

## Cómo usarlo

No necesita configuración. Escribe `/mobile-check` y dale la ruta de tu página (o una URL en vivo). La lee completa a ancho de teléfono y te devuelve una lista numerada ordenada por daño — primero lo que mata la página, al final lo cosmético — más una lista corta de lo que ya pasó la revisión.

Hazlos de a uno. Pega el arreglo #1, mira la página y luego vuelve por el #2. El informe completo se guarda en `~/mobile-checks/`.
