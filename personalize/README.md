# Personalize

Responde un puñado de preguntas una sola vez, y todos los demás skills de este pack escriben con tu voz, para tu oferta, dirigidos a tu audiencia.

Ejecuta este primero. Es el paso de configuración del que dependen los demás skills. Lo único que hace es entrevistarte y guardar las respuestas en un archivo en `~/.claude/brand-profile.md`. Después de eso, **nunca más tienes que explicarte.** Cada skill lee ese archivo automáticamente en lugar de preguntarte quién eres y qué vendes.

## Instalación

1. Copia la carpeta `personalize` en tu directorio de skills de Claude Code:
   ```bash
   cp -r personalize ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/personalize`.

## Cómo usarlo

Escribe `/personalize`. Te hace cinco grupos pequeños de preguntas: tu nombre y a qué te dedicas, a quién intentas llegar, qué vendes, cómo te gusta sonar y cualquier prueba real o links que tengas. Las respuestas cortas están bien. Sáltate lo que todavía no tengas.

Luego escribe `~/.claude/brand-profile.md` y te dice la ruta. No inventará resultados, ingresos ni credenciales. Los espacios vacíos quedan vacíos hasta que los completes. Ejecuta `/personalize` de nuevo cuando quieras para actualizar una sección.
