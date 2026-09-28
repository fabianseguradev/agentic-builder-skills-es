---
name: thread-writer
description: Convierte una idea en un hilo de X o un post largo de LinkedIn que la gente realmente lee hasta el final. Construye un gancho que hace una promesa específica, una idea por línea, un ejemplo real cerca del principio para que confíen en ti, y un final que aterriza en lugar de apagarse. Úsalo cuando el usuario diga "escribe un hilo", "convierte esto en un hilo", "post largo de LinkedIn", "tengo una idea pero es demasiado grande para un post", "cómo explico esto en un post", "redacta esto como un hilo", "convierte esto en una serie de posts" o "/thread-writer".
---

# Thread Writer — una idea, contada para que la terminen

Un hilo falla por una razón: en algún punto del medio, una línea le da permiso al lector para dejar de leer. Este skill construye un hilo donde el único trabajo de cada línea es arrastrarlos hacia la siguiente, abre con una promesa que de verdad cumple y pone algo concreto cerca del principio para que el lector te crea antes de haber invertido ningún tiempo.

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia — yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## Pasos

### 1. Encuentra la ÚNICA idea
Pregunta: "¿Cuál es la única cosa que quieres que alguien se lleve sabiendo?"

Luego comprime su respuesta a una sola oración. Devuélvesela. Si no puedes reducirla a una oración, tienen dos hilos, no uno — haz que elijan cuál escribir ahora.

Pregunta también, si no es obvio: "¿Realmente hiciste esto, o estás explicando algo que leíste?" Un hilo construido sobre su propio proyecto, error o número vale diez construidos sobre consejos generales. Empújalos siempre hacia su propia experiencia.

### 2. Reúne la prueba antes de escribir una palabra
Pide lo concreto:
- un número que realmente midieron (horas, dólares, intentos, usuarios, días)
- un momento específico (la noche en que se rompió, el mensaje del primer usuario)
- un antes y un después que puedan describir

Anota esto primero. Ancla todo el hilo. Si no tienen nada, el hilo va a ser genérico — vuelve atrás y elige una idea más estrecha que realmente hayan vivido.

Nunca inventes un número. Si no hay uno, usa una descripción específica en su lugar: "me tomó cinco noches" es un número; "se seguía colgando en la misma pantalla todas las veces" es un detalle concreto. Ambos funcionan. "Fue muy difícil" no.

### 3. Escribe el gancho con una promesa específica
El gancho es una o dos líneas, y tiene que prometer algo exacto.

Ponlo a prueba contra esto:
- ¿Dice qué obtiene el lector? "Cómo construí un sitio de reservas en un fin de semana sin código" promete. "Algunas reflexiones sobre construir" no.
- ¿Es lo bastante específico como para poder refutarse? Las promesas vagas se leen como ruido.
- ¿Evita el preámbulo? Corta "Quiero hablar de", "Aquí va un hilo sobre", "Déjame contarte".
- ¿Un desconocido que no tiene idea de quién es se detendría por esto?

Una buena forma de gancho: un resultado concreto + la restricción sorprendente. "Construí una app que funciona en 6 noches y todavía no sé leer código."

Escribe tres ganchos. Elige el más fuerte y di por qué en una línea.

### 4. Construye el cuerpo — una idea por línea
Ahora escribe el medio. Las reglas son estrictas porque aquí es donde mueren los hilos.

- **Una idea por línea.** Nunca apiles dos pensamientos en una línea. Si una línea tiene un "y" que une dos ideas, divídela.
- **Una línea en blanco entre cada línea.** El espacio en blanco es lo que lo hace legible en un teléfono.
- **Prueba concreta para la línea 3 o 4.** Pon el número o el momento específico temprano. El lector está decidiendo si confiar en ti en los primeros 15 segundos, no en los últimos.
- **La regla de la retención:** lee cada línea y pregúntate "¿esto hace que necesite la siguiente?" Si una línea resuelve la tensión por completo, mueve la resolución más adelante o córtala. Cada línea termina ligeramente abierta.
- **Nada de resumir a mitad del hilo.** "Como pueden ver" es donde los lectores se van.
- Ordena el medio como una secuencia real: lo que pensaba → lo que pasó → lo que haría distinto. La historia le gana a la lista. Si tiene que ser una lista, haz que cada elemento sea una pequeña historia.

Longitud: de 6 a 12 líneas para X, de 8 a 15 líneas cortas para LinkedIn. Si es más largo que eso, la idea no era una sola idea.

### 5. Aterriza el final
La mayoría de los hilos se apagan en un débil "en fin, espero que ayude." El final debería hacer una de tres cosas, y solo una:
- **Volver de golpe al gancho.** Responder la promesa directamente y detenerse.
- **Entregarles el siguiente paso más pequeño.** Una acción que podrían hacer esta noche, descrita en una línea.
- **Hacer una pregunta real.** No "¿qué opinan?" — algo lo bastante específico como para responder en cinco palabras.

Luego, si hay algo que compartir, un CTA. En X eso es un link o "responde y te lo mando." En LinkedIn, una palabra clave en comentarios atrae más respuestas que un link. Un solo pedido.

### 6. Dale formato a la plataforma y léelo de vuelta
- **X:** no numeres nada. Cada línea se convierte en su propio post del hilo, menos de 280 caracteres cada una. El post 1 es el gancho. El último post carga el CTA.
- **LinkedIn:** un solo post. Las primeras dos líneas tienen que funcionar antes del corte de "ver más" — pon ahí el gancho y la promesa. Mantén cada línea corta.

Revisión final antes de guardar:
- Corta la línea más débil. Siempre hay una.
- Cualquier línea que se pudiera borrar sin perder significado, se borra.
- Palabras prohibidas: desbloquear, apalancar, elevar, revolucionario, viaje, fluido, con humildad, emocionado.
- Léelo en voz alta. Cualquier oración con la que tropieces se reescribe más corta.

## Resultado — guárdalo
Escribe el hilo terminado en `~/threads/YYYY-MM-DD-<short-slug>.md` (crea `~/threads/` si hace falta).

El archivo contiene: la idea de una oración, la plataforma, el gancho elegido más los dos finalistas, el hilo completo con el formato exacto en el que debería publicarse (posts numerados para X, un bloque para LinkedIn) y el CTA.

Dile al usuario la ruta. Luego dale la única siguiente acción: publicarlo, y luego responder a cada comentario en la primera hora — las respuestas son el punto.

## Ejemplo (entrada → salida)
**Entrada:** "Quiero escribir un hilo sobre cómo construí el sitio de mi portafolio en un fin de semana con Claude Code aunque nunca he programado. Me tomó como 9 intentos que el diseño quedara bien."

**Salida (guardada en `~/threads/2026-07-30-portfolio-weekend.md`):**

Una idea: *No necesitas saber programar — necesitas estar dispuesto a decir qué está mal nueve veces.*

Gancho:
> Construí el sitio de mi portafolio en un fin de semana. Nunca he escrito una línea de código.
>
> La parte que nadie te cuenta: me tomó 9 intentos que un diseño quedara bien, y ese es el número normal.

Cuerpo (extracto):
> El intento 1 fue feo. Le dije "el encabezado se siente apretado."
>
> El intento 4 fue peor. Se lo dije también.
>
> Nunca abrí el código. Ni una sola vez.
>
> En cada ronda dije una cosa específica que podía ver con mis propios ojos.
>
> Ese es todo el skill. Describir qué está mal, en voz alta, con palabras normales.

Final:
> El sitio está en línea. Tomó un fin de semana y 9 rondas de mí quejándome en lenguaje simple.
>
> Si has estado esperando a aprender a programar: estás esperando la cosa equivocada.
>
> Comenta SITIO y te mando los prompts exactos que usé.

## Notas / casos especiales
- El error que esto evita: un hilo que en realidad son cinco hilos mezclados. Una idea, o nadie lo termina.
- Si no tienen pruebas, ni un número, ni una historia propia, el hilo va a ser un consejo genérico. Dilo y ayúdalos a estrechar a algo que realmente hicieron.
- Si la idea cabe cómodamente en un solo post, diles que usen **caption-writer** en su lugar. Rellenar una idea pequeña hasta convertirla en hilo es peor que publicar la idea pequeña.
- Si la idea en realidad es un resultado de un cliente, pasa a **case-study** — ese formato convierte mucho mejor para un logro.
- Si el gancho sigue saliendo genérico sin importar cuántos escribas, el problema es el posicionamiento, no el texto. Pasa a **positioning-filter**.
