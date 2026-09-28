# DM Writer

Consigue un mensaje corto para una persona real, escrito con tu voz, que inicie una conversación en lugar de lanzarle un pitch.

Un buen DM no es una difusión masiva. Es un mensaje a *esta* persona, sobre *esta* relación, con una razón para escribir. La regla sobre la que funciona todo el skill: **empieza por ellos.** La primera línea trata de la persona a la que le escribes, no de tu oferta. Una razón, un pedido y una pregunta que puedan responder en una línea.

## Instalación

1. Copia la carpeta `dm-writer` en tu directorio de skills de Claude Code:
   ```bash
   cp -r dm-writer ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/dm-writer`.

## Cómo usarlo

Escribe `/dm-writer` y di a quién le vas a escribir. Te pregunta tres cosas: quién es, qué tan bien lo conoces y qué quieres (iniciar una conversación, compartir tu oferta o hacer seguimiento). Luego escribe un mensaje de 2–5 oraciones que se ajusta a lo cálida que realmente es la relación, más una línea de seguimiento que puedes enviar si no responde. Todo se guarda en `~/dm-drafts.md` para que armes tu propio archivo de referencia.

Lee tu perfil de marca en `~/.claude/brand-profile.md` para escribir con tu voz. Si todavía no lo configuraste, ejecuta `/personalize` primero.
