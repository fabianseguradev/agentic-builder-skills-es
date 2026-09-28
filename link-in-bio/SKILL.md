---
name: link-in-bio
description: Construye tu propia página de link en bio con tu marca en una noche — tu foto, tu nombre, tu pitch de una línea y 4-6 botones en el orden que realmente te hace ganar dinero. Se ve como tú en lugar de como el Linktree de todos los demás, y está hecha primero para el teléfono porque ahí es donde se abre. Úsalo cuando el usuario diga "/link-in-bio", "constrúyeme un link en bio", "necesito un Linktree", "reemplaza mi Linktree", "una página para la bio de mi Instagram", "un link con todos mis links", "página tipo link tree", "link de la bio", "un lugar para poner todos mis links" o "qué pongo en el link de mi bio de Instagram".
---

# Link in Bio — tu propia página, no una alquilada

Tu Linktree se ve igual que el Linktree de todos los demás, y el link más valioso suele estar enterrado al final. Esto construye tu propia página en su lugar: tu cara, tus palabras, tus colores y tus links en un orden deliberado. Es un solo archivo, es tuyo, y nadie pone su logo al final.

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia — yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## Pasos

### 1. Reúne las cuatro piezas
Saca lo que puedas del perfil y pregunta el resto. Mantenlo en una sola ronda corta de preguntas.

- **Foto.** Una foto real de su cara, o su logo si no muestran la cara. Pide la ruta de un archivo en su computadora, o diles que guarden una en `~/sites/<slug>/photo.jpg` y avisen cuando esté ahí. Si ahora no tienen nada, construye con sus iniciales en un círculo y anótalo como algo para arreglar después.
- **Nombre.** Cómo quieren ser conocidos. No su nombre legal, salvo que esa sea la marca.
- **Pitch de una línea.** Qué hacen y para quién, en menos de 12 palabras. No un cargo. "Ayudo a enfermeras a empezar como redactoras freelance" le gana a "Estratega y Consultor de Contenido". Escribe tres opciones y deja que elijan una.
- **Los links.** Pídeles que vuelquen todos los links que querrían ahí, sin filtrar. Espera 8-12. Los vas a recortar.

### 2. Ordena los links — este es el verdadero skill
Dilo claramente: **el orden lo es todo.** La gente escanea los dos primeros botones, toca uno y se va. Cualquier cosa por debajo del botón cuatro es casi invisible en un teléfono. Así que:

Haz el ordenamiento frente a ellos:
1. **El link del dinero va primero.** Lo que sea que lleve a ingresos — la página de reservas, el producto, la comunidad de pago, el formulario de consulta de servicios. No lo gratis. No el canal de YouTube. El link del dinero. Los principiantes lo entierran todas y cada una de las veces por cortesía. Nombra ese hábito en voz alta.
2. **La captura de leads va segunda.** Guía gratuita, newsletter, lista de espera. Así alguien que todavía no está listo para comprar sigue siendo alcanzable.
3. **La mejor prueba va tercera.** Una cosa que demuestre que son reales — un caso de estudio, un portafolio, el mejor video.
4. **Todo lo demás, ordenado según cuánto les ayuda.** Los perfiles de redes sociales van al final, si es que van — la persona ya está en redes; mandarla de vuelta es un bucle.

Luego recorta a **4-6 botones en total.** No más. Pregunta: "Si solo pudieras quedarte con cuatro, ¿cuáles serían?" Borra el resto sin ceremonia. Una página con 11 links es una página donde no se hace clic en nada.

Reescribe cada etiqueta de botón como una acción simple o una cosa simple, no como un nombre de marca. "Agenda una llamada de 20 min" le gana a "Consultoría". "Descarga la checklist gratuita para clientes" le gana a "Recursos gratuitos".

### 3. Construye la página — primero el teléfono, siempre
Di por qué: 95 de cada 100 personas que abren esto están en un teléfono, vienen desde una app y usan un pulgar. Así que está diseñada para el teléfono y simplemente no se rompe en una laptop.

Escribe un solo `index.html` autocontenido:
- Una sola columna, centrada, con un ancho máximo de unos 480px para que siga siendo legible en escritorio en lugar de estirarse.
- Botones a todo el ancho, de al menos 52px de alto, con espacio real entre ellos. Lo bastante grandes para un pulgar, sin hacer zoom, sin nada que se toque por error.
- Todo visible sin scroll en un teléfono normal: foto, nombre, pitch y los dos primeros botones visibles sin desplazarse. Compruébalo.
- Sin herramientas de build, sin librerías de JavaScript externas. Solo Google Fonts — una fuente display para el nombre, una fuente para el cuerpo. Que encajen con su marca.
- Un color de acento más neutros, usado en el botón de arriba para que el link del dinero sea el más llamativo visualmente. Nunca el degradado de IA de morado a azul.
- Animación solo con transforms y opacity — una pequeña elevación o escala al tocar. Sin desenfoque ni ruido animados, sin marquesinas que se desplazan solas.
- Funciona por completo con JavaScript desactivado. Cada botón es un link simple.
- La foto como imagen redonda con una descripción `alt` real. Cualquier ícono como SVG en línea. Texto real, nunca lorem ipsum.
- Un pie de una línea con su nombre y nada más. Sin insignia de "hecho con".

Guarda en `~/sites/<slug>/index.html`, con la foto al lado en la misma carpeta.

### 4. Previsualiza en tamaño de teléfono
Ábrelo:

```bash
open ~/sites/<slug>/index.html
```

Diles que hagan angosta la ventana del navegador — más o menos del ancho de un teléfono — porque juzgarla a ancho completo de escritorio los va a engañar.

Pregunta: "Haz la prueba del pulgar. ¿Puedes tocar cada botón con una mano sin pensar? ¿El botón de arriba parece el más importante?"

Haz el ciclo en palabras simples. Arreglos reales comunes: botones demasiado juntos, nombre demasiado pequeño, foto demasiado grande que empuja los botones fuera de la vista inicial, color de acento demasiado apagado para que destaque el primer botón.

### 5. Guarda las notas y pasa el relevo
Escribe `~/sites/<slug>/NOTES.md` con el orden final de los links y el porqué, más una línea: "Cuando algo cambie, vuelve a ejecutar esto y reordena. El orden debería cambiar a medida que cambia lo que vendes."

Cierra con: "Ejecuta **deploy-it** para tener un link real, y luego pégalo hoy en tu Instagram, tu TikTok y tu firma de email."

## Resultado — guárdalo
- `~/sites/<slug>/index.html` — la página, un archivo, primero el teléfono.
- `~/sites/<slug>/photo.jpg` — su foto, si la aportaron.
- `~/sites/<slug>/NOTES.md` — el orden final de los links con la razón de cada posición.

Indica las rutas. Única siguiente acción: ejecutar **deploy-it** y cambiar el link en su bio.

## Ejemplo (entrada → salida)
**Entrada:** "Hago videos sobre café en casa. Tengo un Linktree con mi YouTube, Instagram, TikTok, mi lista de Amazon, mi newsletter, un Discord y una guía de equipos que vendo a $19."

**Salida (guardada en `~/sites/coffee-page/index.html`):**

Foto. **Sam Ortiz.** "Ayudo a los amantes del café en casa a dejar de desperdiciar buenos granos."

1. **Consigue la guía de equipos de $19** (color de acento, arriba de la página — el link del dinero, antes enterrado bajo tres íconos de redes)
2. **Gratis: mi hoja de referencia de 1 página para calibrar**
3. **Mira: el video del molino (2.1M de vistas)** — solo si ese número es real y es suyo
4. **Únete al Discord**

Lista de Amazon, Instagram y TikTok recortados. `NOTES.md`: "Redes eliminadas — la gente llega desde las redes, mandarla de vuelta es un bucle. Revisar cuando la guía se convierta en un curso."

## Notas / casos especiales
- El error que esto evita: un muro de links que se ven todos iguales donde lo que paga es lo que menos se toca. Si se niegan a poner primero el link del dinero, pídeles que lo prueben dos semanas y comparen la diferencia.
- Si todavía no tienen un link del dinero, pon primero la captura de leads y anota en `NOTES.md` que la posición uno está reservada para lo que vendan después. Pasa a **offer-builder**.
- Si solo tienen dos links, está bien — construye los dos. Rellenar con relleno lo empeora.
- Nunca escribas cantidades de seguidores, de vistas ni de clientes que no te dieron. Pregunta, o déjalo fuera.
- Derivación: **deploy-it** para publicar. **positioning-filter** si el pitch de una línea sigue saliendo genérico. **landing-page** si uno de los botones merece una página propia de verdad.
