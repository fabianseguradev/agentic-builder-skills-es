# Waitlist Page

Un "próximamente" de una página que recolecta emails esta noche, para que averigües si alguien quiere la cosa antes de pasar tres meses construyéndola.

El error caro es construir primero y preguntar después. Veinte personas que escribieron su email es información real. Doce amigos diciendo "buena idea" no lo es. Esto construye una página con **una promesa, un campo, un botón y una fecha honesta** — más un lugar gratuito real donde llegan los emails, para que no desaparezcan.

## Instalación

1. Copia la carpeta `waitlist-page` en tu directorio de skills de Claude Code:
   ```bash
   cp -r waitlist-page ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/waitlist-page`.

## Cómo usarlo

Ejecuta `/personalize` primero para que la página suene a ti. Luego escribe `/waitlist-page` y responde cuatro preguntas: qué es la cosa, para quién es, qué les da y para cuándo estará lista de verdad.

Eliges una línea de promesa entre tres opciones y eliges dónde llegan los emails (Google Form, nivel gratuito de Formspree o un mailto simple). Obtienes una página terminada en `~/sites/<name>-waitlist/index.html` más un archivo de notas con tu regla de decisión — cuántos registros significan construirlo, y cuán pocos significan que no.
