# Landing Page

Un sitio de una página cuyo único trabajo es conseguirte un email o una reserva — titular, tres pruebas, un formulario, un botón y unas preguntas frecuentes que eliminan la objeción más grande.

La columna vertebral de este skill es **la Regla de Un Solo Trabajo**: una página que pide dos cosas no consigue ninguna. Sin barra de navegación, sin íconos de redes sociales, sin segunda oferta. Todo lo que no empuja hacia la acción única sale de la página. También conecta el formulario a un servicio gratuito para que los emails realmente lleguen a tu bandeja de entrada en lugar de desaparecer.

## Instalación

1. Copia la carpeta `landing-page` en tu directorio de skills de Claude Code:
   ```bash
   cp -r landing-page ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/landing-page`.

## Cómo usarlo

Ejecuta `/personalize` primero para que la página suene a ti. Luego escribe `/landing-page` y di qué quieres que haga la gente — unirse a una lista, descargar una guía gratuita, agendar una llamada.

Te pregunta para quién es, cuál es el único resultado, tres pruebas reales y la razón más grande por la que alguien cerraría la pestaña. Luego escribe el texto, construye un solo `index.html` autocontenido y te muestra la página para que puedas reaccionar con palabras simples. Obtienes un archivo funcionando en `~/sites/<your-project>/index.html`. Ejecuta `/deploy-it` para ponerlo en un link real.
