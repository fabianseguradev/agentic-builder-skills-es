# First Website

Construye tu primer sitio web real describiendo en voz alta lo que quieres — sin código, sin configuración, un solo archivo que se abre en tu navegador.

Aquí no estás aprendiendo a programar. Estás aprendiendo a dirigir. El skill lleva tu idea de vaga a **quirúrgica** — quién es el visitante, la única acción que quieres, la sensación, las restricciones firmes — y luego construye una versión que puedes mirar y a la que puedes reaccionar con palabras normales. Cinco a diez rondas de eso son todo el flujo de trabajo, no una señal de que lo estás haciendo mal.

## Instalación

1. Copia la carpeta `first-website` en tu directorio de skills de Claude Code:
   ```bash
   cp -r first-website ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/first-website`.

## Cómo usarlo

No necesita configuración. Escribe `/first-website` y describe el sitio que quieres, por desordenado que sea. Te hace algunas preguntas cortas, construye un solo `index.html` autocontenido, lo abre para que lo veas y luego pregunta "¿qué es lo primero que te molesta?". Respondes en lenguaje simple, lo arregla, vuelves a mirar.

Terminas con un archivo real en `~/sites/<your-project>/index.html` más un archivo corto de notas para mañana. Luego ejecuta `/deploy-it` para ponerlo en una dirección web real y mándale el link a una persona hoy.
