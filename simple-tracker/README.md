# Simple Tracker

Un pequeño tracker personal que funciona en tu navegador y se guarda en tu propia máquina — hábitos, entrenamientos, clientes, libros, dinero que entra. Un archivo, sin login, sin base de datos, sin factura mensual.

Lo que la mayoría de la gente quiere de una app es una lista a la que pueda agregar cosas y un número que le diga cómo va. Eso no necesita un backend. Todo buen tracker pequeño tiene las mismas tres partes: **una cosa que agregas, una lista que ves, un número arriba.** Construye eso, úsalo una semana, y luego cambia la única cosa que te molestó.

## Instalación

1. Copia la carpeta `simple-tracker` en tu directorio de skills de Claude Code:
   ```bash
   cp -r simple-tracker ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/simple-tracker`.

## Cómo usarlo

No necesita configuración. Escribe `/simple-tracker` y di qué quieres rastrear. Si no estás seguro, te da seis ideas — tracker de hábitos, registro de entrenamientos, pipeline de clientes, lista de lectura, dinero que entra, registro de contenido — cada una con un texto de partida.

Obtienes un archivo funcionando en `~/tools/<name>/index.html`. Márcalo como favorito, o agrégalo a la pantalla de inicio de tu teléfono para que se abra como una app. Tus datos se guardan en tu navegador, y la página incluye botones de exportar e importar para que puedas respaldarlos y moverlos.
