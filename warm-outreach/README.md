# Warm Outreach

Construye una lista ordenada de personas que ya te conocen, más un primer mensaje que inicia una conversación en lugar de lanzarle un pitch a un amigo.

Tu primer cliente casi nunca viene de un desconocido. Viene de un cliente anterior, un excompañero de trabajo, alguien de un grupo en el que ya estás, o la persona que le da like a cada post que haces. La regla aquí es **cálido antes que frío, honesto antes que insistente.** No le estás mandando spam a nadie. Estás hablando con personas reales.

## Instalación

1. Copia la carpeta `warm-outreach` en tu directorio de skills de Claude Code:
   ```bash
   cp -r warm-outreach ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/warm-outreach`.

## Cómo usarlo

Escribe `/warm-outreach`. Lee tu perfil de marca en `~/.claude/brand-profile.md`, así que ejecuta `/personalize` primero si no lo has hecho. Te guía grupo por grupo por todos los que te conocen, apuntando a entre 20 y 40 nombres, y luego puntúa a cada uno en encaje y calidez para que sepas a quién escribirle primero y a quién pedirle una referencia en su lugar.

Obtienes la tabla ordenada y tres variaciones de apertura (reconectar, señal suave, pedido de referencia) guardadas en `~/warm-outreach-list.md`, cada una con un espacio entre corchetes para el detalle personal que completas por persona. Manda a los cinco primeros esta semana, no toda la lista.
