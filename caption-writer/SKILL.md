---
name: caption-writer
description: Consigue un caption listo para publicar sobre algo que construiste, hiciste o aprendiste — escrito con tu voz, con la longitud correcta para Instagram, LinkedIn, X o TikTok. Elige una de cuatro formas de post que realmente funcionan y escribe una primera línea que detiene el scroll. Úsalo cuando el usuario diga "escribe un caption", "caption para este post", "construí algo, qué digo", "cómo publico sobre esto", "escribe el texto de mi post de Instagram", "no sé cómo hablar de lo que hice", "ayúdame a publicar esto sin sonar vendedor" o "/caption-writer".
---

# Caption Writer — publica sobre lo que hiciste sin sonar a anuncio

La mayoría de la gente construye algo y luego se queda callada, porque escribir sobre ello se siente como presumir. La solución es dejar de anunciarte a ti mismo y empezar a mostrar la cosa. Este skill elige la forma de post correcta, escribe una primera línea que hace todo el trabajo y guarda un caption terminado que puedes pegar y publicar.

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia — yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## Pasos

### 1. Consigue la materia prima
Pide lo que tengan, en palabras simples. Dos preguntas, como máximo:
- "¿Qué es la cosa? Dime qué es y qué hace, como si le escribieras a un amigo."
- "¿Hay un link, una captura de pantalla o un video? ¿Y en qué plataforma se va a publicar?"

Si divagan, está bien — las mejores líneas suelen estar ya en su divagación. Toma las frases exactas que usaron y consérvalas. No limpies sus palabras hasta convertirlas en lenguaje de marketing.

Si solo tienen un vago "he estado trabajando en cosas", haz una pregunta más: "¿Qué cambió hoy que no existía ayer?" Esa respuesta es el post.

### 2. Elige la forma del post
Elige UNA de cuatro. Di cuál elegiste y por qué, en una línea. Nunca mezcles dos.

- **Mostrar la cosa.** Ideal cuando hay una captura, un video o un link en vivo. El trabajo del caption es pequeño: decir qué es, para quién es y un detalle honesto sobre cómo se hizo. Lo visual sostiene el post.
- **La lección de un error.** Ideal cuando algo se rompió, tomó cinco intentos o estaban equivocados sobre algo. La que más confianza genera de las cuatro. Estructura: lo que creía → lo que realmente pasó → lo que haría ahora.
- **Antes y después.** Ideal cuando hay un cambio visible o medible: página vieja vs página nueva, 3 horas vs 10 minutos, lista vacía vs 40 personas. Necesita un contraste real, no una sensación.
- **Actualización honesta de progreso.** Ideal cuando nada está terminado. Este es el post de construir en público. Estructura: dónde está ahora mismo → la única parte difícil → qué sigue. Lo inacabado está permitido. Lo falsamente terminado, no.

### 3. Escribe la primera línea
La primera línea es todo el post. En todas las plataformas, es la única línea que la mayoría ve antes de decidir.

Reglas:
- Nada de rodeos. Aperturas prohibidas: "Emocionado de compartir", "Me complace anunciar", "Estuve pensando", "Hola a todos", "Post rápido sobre".
- Empieza en el momento más filoso. Quita la oración de calentamiento y abre con la segunda oración que habrías escrito.
- Sé específico y concreto. "Construí una herramienta que te dice si tu alquiler es demasiado alto" le gana a "Construí algo de lo que estoy orgulloso".
- Un número, un detalle raro o una confesión funcionan. El ingenio normalmente no.

Escribe tres primeras líneas candidatas. Muéstraselas al usuario, elige tú la más fuerte y di por qué en una línea. Pueden cambiarla.

### 4. Escribe el cuerpo para la plataforma
Una idea por línea. Línea en blanco entre líneas. Nada de bloques de párrafo.

Ajústalo a la plataforma:
- **Instagram** — de 4 a 8 líneas cortas. La primera línea tiene que funcionar antes del corte de "más". Conversacional. Hasta 5 hashtags al final de todo, simples y específicos, sin sopa de hashtags.
- **LinkedIn** — de 6 a 12 líneas cortas. La misma voz, con un poco más de contexto sobre a quién ayuda y por qué importa. Sin registro corporativo, nada de "con humildad". Las primeras 2 líneas se ven antes del corte de "ver más".
- **X** — menos de 280 caracteres, o un único post ajustado. Quita cada palabra que no sostenga peso. Sin hashtags.
- **TikTok** — solo 1 o 2 líneas. El caption acompaña al video, no lo repite. Agrega una pregunta que invite a comentar.

### 5. Agrega el CTA
Si hay un link de por medio, NO pongas un link directo en el post en Instagram ni en TikTok — mata el alcance y de todos modos nadie puede tocarlo. Usa una palabra clave en los comentarios:

> Comenta JUEGO y te mando el link.

Elige una palabra clave que sea una sola palabra, en mayúsculas y relacionada con la cosa (JUEGO, HERRAMIENTA, SITIO, PRESUPUESTO, SEGUIMIENTO). Los comentarios se convierten en conversaciones, y las conversaciones son donde la gente realmente compra. En LinkedIn y X un link en el post está bien, pero una palabra clave igual consigue más respuestas.

Si no hay link, termina con una pregunta real que de verdad responderían — sobre la cosa, no "¿qué opinan?". Algo como "¿Qué te gustaría que hiciera después?"

Un CTA por post. Nunca dos.

### 6. Léelo en voz alta
Antes de guardar, haz esta revisión al borrador:
- ¿La primera línea hace que alguien se detenga, sin contexto?
- ¿Hay alguna línea que solo existe para sonar impresionante? Quítala.
- ¿Le dirían esta oración a un amigo en la mesa? Si no, reescríbela.
- ¿Alguna de estas palabras? desbloquear, apalancar, elevar, revolucionario, viaje, emocionado, con humildad. Quítalas.
- ¿Hay exactamente un pedido?

## Resultado — guárdalo
Escribe el caption terminado en `~/captions/YYYY-MM-DD-<short-slug>.md` (crea `~/captions/` si hace falta).

El archivo contiene: la plataforma, la forma de post elegida, el caption final exactamente como debe pegarse (en un bloque listo para copiar), las dos primeras líneas finalistas y la palabra clave para comentarios si la hay.

Dile al usuario la ruta. Luego dile la única siguiente acción: publicarlo y responder a cada comentario durante la primera hora.

## Ejemplo (entrada → salida)
**Entrada:** "Hice un pequeño juego de navegador donde esquivas emails que caen. Es tonto pero funciona y está en línea. Lo voy a publicar en Instagram."

**Salida (guardada en `~/captions/2026-07-30-email-dodge-game.md`):**

Forma: Mostrar la cosa.

> Hice un juego donde esquivas emails que caen y es genuinamente estresante.
>
> Empezó como una broma sobre mi bandeja de entrada.
>
> Me tomó cuatro noches. Casi todo eso fue hacer que los emails cayeran a una velocidad que se sintiera cruel pero justa.
>
> Funciona en tu navegador. Sin descargas, sin registro.
>
> Comenta JUEGO y te mando el link.

Primeras líneas finalistas: "Mi bandeja de entrada se convirtió en un videojuego." / "Cuatro noches de trabajo para que los emails que caen se sientan crueles pero justos."

## Notas / casos especiales
- El error que esto evita: escribir un caption que describe cómo se siente la persona en lugar de mostrar lo que hizo. Los sentimientos no viajan. La cosa sí.
- Si no han construido nada ni aprendido nada, no escribas un post. Díselo. Un post vacío cuesta más que no publicar.
- Si la entrada es escasa, usa "Actualización honesta de progreso" — es la única forma que funciona con algo inacabado, y la que más probabilidades tiene de conseguir respuestas reales.
- Si ni siquiera saben para quién es el post, o cada caption suena como el de todos los demás, detente y pasa primero a **positioning-filter**.
- Si la idea es más grande que un caption — tres o más puntos distintos — pasa a **thread-writer** en lugar de meterlo todo a presión.
- Nunca inventes una métrica. "Ahora es más rápido" está bien. "Es un 40% más rápido" solo está bien si lo midieron.
