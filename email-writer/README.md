# Email Writer

Escribe el email que has estado evitando — el cobro de una factura, el no, la disculpa, el tercer seguimiento.

Los emails difíciles no se envían porque la gente no encuentra el tono, así que escriben cuatro párrafos de preámbulo y esconden el pedido real en la última línea. Este skill le da la vuelta: **un pedido, cerca del principio**, en palabras cortas y simples que siguen sonando a ti.

## Instalación

1. Copia la carpeta `email-writer` en tu directorio de skills de Claude Code:
   ```bash
   cp -r email-writer ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/email-writer`.

## Cómo usarlo

Ejecuta `/personalize` primero para que el email suene a ti. Luego escribe `/email-writer` y describe la situación con tus propias palabras — "un cliente me debe dinero y ya le insistí una vez" es suficiente.

Te pregunta tres cosas: quién es esta persona para ti, qué quieres que pase y qué tan directo puedes ser. Luego te entrega un asunto y un cuerpo corto con el pedido arriba, más una versión más cálida y otra más firme de la línea más arriesgada para que ajustes el tono sin reescribir. Todo se guarda en `~/emails/`.
