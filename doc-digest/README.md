# Doc Digest

Apúntalo a un documento largo y recibe las decisiones, los números, las fechas y las trampas.

Los documentos largos esconden las partes caras en el medio. Este skill lee todo y extrae lo que importa, con una línea firme entre **lo que dice y lo que deberías hacer al respecto** — citas de un lado, tus opciones del otro, para que nunca confundas las dos cosas.

## Instalación

1. Copia la carpeta `doc-digest` en tu directorio de skills de Claude Code:
   ```bash
   cp -r doc-digest ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/doc-digest`.

## Cómo usarlo

No necesita configuración. Escribe `/doc-digest` y dale una ruta de archivo, una URL o simplemente pega el texto. Hace una pregunta — si lo vas a firmar, responder, si vas a decidir algo o solo quieres entenderlo — porque eso cambia lo que extrae.

Recibes un resumen de una página guardado en `~/digests/`: qué es el documento, qué te pide, cada número y cada fecha, las cláusulas que vale la pena vigilar, lo que falta de forma sospechosa y las preguntas exactas para enviar antes de firmar. No te dará asesoría legal ni financiera — señala las partes que vale la pena poner frente a un profesional.
