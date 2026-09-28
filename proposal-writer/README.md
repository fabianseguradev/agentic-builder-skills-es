# Proposal Writer

Entran notas desordenadas de una llamada. Sale una propuesta limpia y lista para enviar, guardada como un archivo que puedes pegar directamente en un email.

Una propuesta no es una lista de precios con tu nombre. Es un documento corto que demuestra que entendiste el problema, muestra lo que cambia cuando se resuelve y pone el precio cuando el comprador ya quiere la cosa. **Primero el valor, después el número.** Si aciertas con ese orden, el precio deja de ser la parte que da miedo.

## Instalación

1. Copia la carpeta `proposal-writer` en tu directorio de skills de Claude Code:
   ```bash
   cp -r proposal-writer ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/proposal-writer`.

## Cómo usarlo

Ejecuta `/personalize` una vez primero para que escriba con tu voz. Luego escribe `/proposal-writer` y pega lo que tengas de la llamada. Unas viñetas rápidas están bien.

Extrae las tres cosas sin las que no puede escribir (su problema, lo que vas a entregar, tu precio) y pregunta si falta alguna. No va a adivinar un número ni a inventar un alcance. Luego escribe el documento: su situación con sus propias palabras, el resultado, exactamente lo que obtienen, los plazos, una tabla de precios con dos opciones y una marcada como recomendada, tu garantía si tienes una y un único siguiente paso claro en lugar de "avísame".

Terminas con un archivo en `~/proposals/proposal-<client>-<date>.md`, más un email corto para enviarlo.
