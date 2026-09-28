# Skill Starter

Convierte un trabajo que le sigues pidiendo a Claude en tu propio comando de barra.

El disparador es simple: **le has pedido el mismo tipo de cosa dos o tres veces.** Ese es el momento de embotellarlo. Este skill te entrevista sobre el trabajo, los pasos y las palabras que de verdad escribirías para pedirlo — y luego escribe un skill funcional que puedes ejecutar para siempre. Es el que te convierte de alguien que usa los skills de otros en alguien que hace los suyos.

## Instalación

1. Copia la carpeta `skill-starter` en tu directorio de skills de Claude Code:
   ```bash
   cp -r skill-starter ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/skill-starter`.

## Cómo usarlo

No necesita configuración. Escribe `/skill-starter` y describe el trabajo que sigues repitiendo. Pregunta qué entra y qué sale, cómo formularías el pedido con tus propias palabras descuidadas, los pasos que seguirías a mano y dónde debería guardarse el resultado. Luego escribe un `SKILL.md` en `~/.claude/skills/<your-slug>/`.

Reinicia Claude Code y escribe `/<your-slug>`. Si no aparece, no reiniciaste — los skills solo se cargan cuando arranca una sesión.
