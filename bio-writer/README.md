# Bio Writer

La bio de tu perfil escrita para cada plataforma con la longitud correcta, a partir de lo que realmente haces y de una cosa real que hayas hecho.

Una bio tiene dos segundos para hacer un solo trabajo. **Hacer que la persona correcta se quede y la equivocada se vaya.** La mayoría de las bios fallan por intentar agradar a ambos, y así es como terminas "apasionado por ayudar a los negocios a crecer". Esta dice qué haces, para quién es y una prueba específica — nada más.

## Instalación

1. Copia la carpeta `bio-writer` en tu directorio de skills de Claude Code:
   ```bash
   cp -r bio-writer ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/bio-writer`.

## Cómo usarlo

Ejecuta `/personalize` una vez primero para que tenga tu nicho, tu oferta y tu audiencia. Luego escribe `/bio-writer`.

Toma lo que puede de tu perfil, pregunta lo que falte y comprueba que tu ángulo sea lo bastante afilado como para que valga la pena escribirlo — si no lo es, te dirá que ejecutes `/positioning-filter` primero en lugar de escribirte una mala bio bien pulida. Obtienes cinco versiones con conteo de caracteres: Instagram (150), titular de LinkedIn (220) más una sección Acerca de completa, X (160) y una frase de una línea para tu link en bio o tu firma de email. Guardado en `~/brand/bio.md`.
