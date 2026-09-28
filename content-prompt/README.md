# Content Prompt Generator

Consigue una pregunta que valga la pena responder frente a cámara, más cinco ganchos y textos en pantalla, para que puedas presionar grabar sin quedarte mirando una página en blanco.

La mayoría de los consejos de formato corto te dicen que comentes lo que está en tendencia. Esto hace lo contrario: **la tendencia es la puerta, tu historia es la habitación.** El skill encuentra una tensión viva en tu nicho, la conecta con algo que viviste de verdad — un error, un punto de inflexión, un resultado que te sorprendió — y construye el disparador alrededor de eso.

## Instalación

1. Copia la carpeta `content-prompt` en tu directorio de skills de Claude Code:
   ```bash
   cp -r content-prompt ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/content-prompt`.

## Cómo usarlo

Lee tu perfil de marca en `~/.claude/brand-profile.md`, así que ejecuta `/personalize` primero si no lo has hecho. De ahí saca tu audiencia, tu punto de dolor, tu prueba real y tu tono.

Escribe `/content-prompt`. Recibes una pregunta, la semilla de la historia de la que sale, por qué es oportuna, cinco ganchos (cada uno con su propio texto en pantalla), una recomendación de qué gancho usar y un CTA para seguir. Si tu perfil tiene pocos momentos reales, te pide uno y lo guarda.
