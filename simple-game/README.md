# Simple Game

Construye un juego de navegador jugable en una sola sentada — un archivo, se abre en cualquier lugar, funciona en un teléfono, nada que instalar.

Un juego es la mejor primera construcción porque **no te puedes mentir a ti mismo sobre si funciona.** Presionas una tecla y la cosa se mueve o no se mueve. La gente también de verdad juega juegos — mándale a alguien un sitio web y recibes "lindo", mándale un juego y recibes su puntaje de vuelta. Y es un solo archivo autocontenido sin base de datos, sin login y sin servidor.

## Instalación

1. Copia la carpeta `simple-game` en tu directorio de skills de Claude Code:
   ```bash
   cp -r simple-game ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/simple-game`.

## Cómo usarlo

No necesita configuración. Escribe `/simple-game` y recibes un menú de unos ocho clásicos etiquetados según cuánto toman — 15 minutos, una hora, una noche. Elige uno, o nombra un juego que te encantaba.

Escribe una especificación de cuatro partes contigo primero (contenedor, una regla de jugabilidad por viñeta, ubicación de la UI y "muéstrame una vista previa en vivo"), lo construye y lo abre para que juegues. Reaccionas en palabras simples durante algunas rondas hasta que se siente bien. Luego hace la pasada de "hazlo tuyo": le cambia la temática a algo de tu vida, agrega exactamente un giro, pone tu nombre en la pantalla de título, guarda el puntaje máximo, agrega un botón de compartir.

Obtienes un archivo jugable en `~/games/<your-game>/index.html`. Ejecuta `/deploy-it` para conseguir un link y mándaselo a tres personas esta noche.
