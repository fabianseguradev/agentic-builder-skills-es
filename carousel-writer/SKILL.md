---
name: carousel-writer
description: Consigue las palabras exactas para cada slide de un post en carrusel, más una nota breve de qué va visualmente en cada slide, para que puedas armarlo en Canva o hacer que Claude lo construya como una página web. El slide 1 funciona como gancho por sí solo, una idea por slide, de 7 a 10 slides, el último slide es el pedido. Úsalo cuando el usuario diga "escribe un carrusel", "post en carrusel sobre", "convierte esto en slides", "post para deslizar", "necesito el texto de mi carrusel", "haz de esto un post de 10 slides", "qué pongo en cada slide" o "/carousel-writer".
---

# Carousel Writer — las palabras para cada slide, en orden

Los carruseles se guardan y se comparten más que cualquier otro post, y la gente los arruina poniendo un párrafo en el slide uno. Este skill escribe el texto slide por slide, con la menor cantidad posible de palabras en cada uno, y trata el slide 1 como un trabajo aparte: la mayoría de la gente solo verá ese slide. Escribe las palabras. No hace las imágenes.

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia — yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## Pasos

### 1. Fija la idea única y la promesa
Pregunta dos cosas:
- "¿Cuál es la idea única? Dila en una oración."
- "¿Qué debería poder HACER alguien después de deslizar esto?"

Si la respuesta a la segunda es "saber más sobre mí", detente. Eso no es un carrusel, es una bio. Insiste hasta que la respuesta sea algo que puedan hacer o usar.

Luego decide el tipo de carrusel y di cuál elegiste:
- **La lista** — de 5 a 7 cosas, una por slide. La más fácil de guardar, la más fácil de hacer.
- **El paso a paso** — los pasos de algo que hicieron, en orden. Ideal cuando construyeron algo.
- **El error** — lo que la mayoría hace mal, por qué falla, qué hacer en su lugar.
- **El antes/después** — la forma vieja vs la forma nueva, lado a lado a lo largo de los slides.

### 2. Escribe el slide 1 como si fuera el único slide
El slide 1 es todo el post. Si falla, no se ve nada más.

Reglas:
- **Menos de 10 palabras.** Idealmente menos de 7. Si necesita una segunda oración, no está lo bastante afilado.
- Tiene que hacer una promesa o una afirmación, no describir un tema. "5 herramientas gratis que uso todos los días" le gana a "Reflexiones sobre mis herramientas".
- Sin nombre, sin logo, sin "desliza →" en el slide 1. Dale a las palabras todo el cuadro.
- Lo bastante grande como para leerse como miniatura con el teléfono a la distancia del brazo.

Escribe tres versiones del slide 1. Elige la más fuerte, di por qué en una línea y guarda las otras dos en el archivo.

### 3. Escribe los slides del medio
Una idea por slide. Esta es la regla de la que depende todo lo demás.

Para cada slide escribe:
- **Titular:** de 3 a 8 palabras. Esto es lo que leen.
- **Línea de apoyo (opcional):** una oración corta, solo si el titular de verdad no se sostiene solo. La mayoría de los slides no la necesitan. Bórrala si tienes dudas.
- **Nota visual:** una línea que les dice qué va en el slide — una captura de la cosa, un número grande, una división en dos columnas, una flecha o solo las palabras sobre un fondo liso. Palabras sobre un fondo liso es una respuesta legítima y muchas veces la mejor.

Límites estrictos:
- Máximo 20 palabras de texto en un solo slide, incluida la línea de apoyo.
- Nunca dos ideas en un slide. Si hay una "y", divídelo en dos slides.
- El slide 2 debería entregar la primera pieza de valor de inmediato. Nada de slide de "esto es lo que vamos a ver" — es un slide en el que la gente deja de deslizar.
- Mantén un hilo que tire hacia adelante. Cada slide debería dejar el siguiente con ganas de deslizar.

Total: de 7 a 10 slides, incluidos el slide 1 y el slide del CTA. Menos de 7 se siente flojo. Más de 10 pierde a la gente.

### 4. Pon algo concreto en el medio
En algún lugar entre los slides 3 y 6, un slide debería llevar una prueba: un número real, una captura de lo que construyeron, un antes/después real o un momento específico. Este es el slide que hace creíble todo el carrusel.

Nunca inventes el número. Si no hay uno, usa una captura o una descripción concreta en su lugar.

### 5. Escribe el último slide — el CTA
El último slide hace un solo trabajo. Un pedido, nunca dos.

Elige el adecuado:
- **Palabra clave en comentarios** — ideal cuando hay un link, una plantilla o un archivo para enviar. "Comenta HERRAMIENTAS y te mando la lista." Una palabra, en mayúsculas.
- **Seguir** — ideal cuando todavía no hay nada que enviar. Di qué obtendrán si lo hacen, de forma específica. "Publico un proyecto por semana — sígueme si estás construyendo algo."
- **Guardar** — ideal en un carrusel de lista o de referencia. "Guarda esto para la próxima vez que te trabes."

Escríbelo en palabras simples. Nada de energía de "¡¡link en la bio!!", sin signos de exclamación.

### 6. Escribe la instrucción para armarlo
Como este skill solo escribe palabras, termina dándoles una instrucción lista para usar para hacerlo de verdad. Incluye ambas opciones en el archivo de salida:

**Ruta Canva:** una línea por slide que puedan copiar en cuadros de texto, más una nota: elige una fuente display en negrita para los titulares y una fuente simple para las líneas de apoyo, un color de acento más neutros, y mantén el diseño de cada slide idéntico salvo el texto.

**Ruta Claude:** un prompt listo para copiar que puedan pegar en una sesión nueva de Claude Code, escrito para ellos, más o menos así:

> Constrúyeme un carrusel en un solo `index.html` autocontenido con 9 slides, de 1080x1350 cada uno, al que pueda sacarle captura uno por uno. Sin herramientas de build y sin librerías de JavaScript. Usa solo Google Fonts — una fuente display en negrita para los titulares, una fuente simple para el cuerpo. Un color de acento más neutros, sin degradado de morado a azul. Todos los slides tienen el mismo diseño: titular grande y centrado, línea de apoyo opcional debajo, mucho espacio vacío. Este es el texto exacto de cada slide: [pega el texto de los slides]. Agrega las flechas izquierda/derecha del teclado para moverse entre slides. Haz que se pueda leer con JavaScript desactivado.

### 7. Revisión final
- Lee solo los titulares, en orden, de arriba a abajo. ¿Cuentan toda la historia por sí solos? Si no, los titulares son demasiado vagos.
- Quita el slide más débil. Siempre hay uno.
- Cualquier slide de más de 20 palabras se recorta o se divide.
- Palabras prohibidas: desbloquear, apalancar, elevar, revolucionario, fluido, viaje, empoderar.

## Resultado — guárdalo
Escribe el resultado en `~/carousels/YYYY-MM-DD-<short-slug>.md` (crea `~/carousels/` si hace falta).

El archivo contiene: la idea única, el tipo de carrusel, cada slide numerado con su titular / línea de apoyo / nota visual, las dos opciones finalistas del slide 1, el caption para publicarlo (de 2 a 4 líneas cortas, no una repetición de los slides) y ambas rutas para armarlo, incluido el prompt de Claude listo para copiar.

Dile al usuario la ruta y luego la única siguiente acción: armar primero el slide 1 y mirarlo en tu teléfono antes de armar el resto.

## Ejemplo (entrada → salida)
**Entrada:** "Quiero un carrusel sobre los errores que cometí construyendo mi primer sitio web con IA. Fueron como 5 grandes."

**Salida (guardada en `~/carousels/2026-07-30-first-site-mistakes.md`):** Tipo: el error. 8 slides.

- **1.** `5 errores que cometí construyendo mi primer sitio` — solo palabras, fondo liso, tipografía enorme.
- **2.** `Pedí "una página de inicio bonita"` / *Apoyo:* "Obtuve exactamente lo que eso significa: nada." — solo palabras.
- **3.** `Entra algo vago, sale algo vago` / *Apoyo:* "Di quién visita, en qué quieres que haga clic y cómo debería sentirse." — solo palabras.
- **4.** `Intenté arreglar el código yo mismo` / *Apoyo:* "No leo código. Lo rompí peor." — captura de la página rota.
- **5.** `Tomó 9 rondas. Es normal.` — número 9 grande llenando el slide.
- **6.** `Esperé hasta que quedara bonito` / *Apoyo:* "Feo y en línea le gana a perfecto y en mi laptop." — división antes/después.
- **7.** `No le conté a nadie que lo hice` — solo palabras.
- **8.** `Comenta SITIO y te mando los prompts que usé.` — solo palabras, color de acento.

## Notas / casos especiales
- Este skill escribe texto y describe slides. No genera imágenes. Dilo claramente si esperaban imágenes.
- El error que esto evita: un muro de texto en el slide 1 que nadie lee, seguido de 9 slides que nadie ve.
- Si la idea no sobrevive a recortarse a 8 palabras por slide, no es una idea de carrusel. Pásala a **thread-writer** — algunas ideas necesitan oraciones.
- Si tienen 15 puntos, tienen dos carruseles. Haz que elijan los 7 más fuertes y guarden el resto.
- Si todos los titulares suenan como los de todos los demás, el problema es el ángulo. Pasa a **positioning-filter**.
- Nunca fabriques un slide de prueba. Una captura de algo a medio terminar vale más que un número inventado.
