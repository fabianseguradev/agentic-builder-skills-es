---
name: waitlist-page
description: Construye un "próximamente" de una página que recolecta emails antes de que la cosa exista, para que averigües si alguien la quiere antes de pasar tres meses construyéndola. Una promesa, un campo, un botón, una fecha honesta y un lugar real donde llegan los emails — todo gratis, sin backend. Úsalo cuando el usuario diga "construye una página de lista de espera", "página de próximamente", "recolecta emails antes de construir", "quiero ver si alguien quiere esto", "landing page para una idea", "página de prelanzamiento", "valida mi idea", "registro de acceso anticipado", "debería construir esto primero" o escriba /waitlist-page.
---

# Waitlist Page — prueba de demanda antes de construir

El error caro es construir durante tres meses y luego descubrir que nadie lo quería. La versión barata es una página, lista esta noche, que dice qué es la cosa y pide un email. Veinte personas que escribieron su dirección de email es información real. Doce amigos diciendo "buena idea" no lo es. Esto construye esa página, la pone en algún lugar real y te dice exactamente dónde llegan los emails.

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia — yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## Pasos

### 1. Consigue la promesa, y hazla específica
Lee el perfil de marca para saber a quién sirven y qué hacen. Luego haz exactamente cuatro preguntas en un solo mensaje:

1. "¿Qué es la cosa, en una oración que un desconocido entendería?"
2. "¿Para quién es, específicamente? No 'pequeñas empresas' — 'peluqueros caninos independientes con 10-40 clientes'."
3. "¿Cuál es la única cosa que les da que hoy no pueden conseguir fácilmente?"
4. "¿Para cuándo crees honestamente que va a estar listo? Un mes aproximado está bien. Una mentira no."

Luego escribe la línea de la promesa. Esto es toda la página. Reglas:
- Nombra a la persona y el resultado. "Una página de reservas para peluqueros caninos independientes que termina con el ida y vuelta de mensajes de texto" le gana a "el futuro de la programación."
- Menos de 15 palabras si puedes.
- Sin adjetivos exagerados. Si la promesa necesita un adjetivo para sonar bien, la promesa es débil.
- Ponla a prueba: ¿alguien con este problema exacto dejaría de scrollear? Si no, reescríbela con una persona más específica.

Dales tres versiones de la línea de la promesa y haz que elijan una. Elegir es más rápido que escribir.

### 2. Decide dónde llegan realmente los emails — antes de construir la página
Este es el paso que la gente se salta, y luego los emails no llegan a ningún lado. Dales estas tres opciones gratuitas, di qué le cuesta a cada una en esfuerzo y haz que elijan una:

- **Google Form (cero registro si tienen Gmail, la opción por defecto recomendada).** Hacen un Google Form con un campo de email, y luego el botón de la página lleva directo ahí, o la página envía a la URL del formulario. Los emails llegan a una Hoja de Google que ya es suya. Gratis para siempre, sin límites que preocupen. Desventaja: si el botón solo enlaza hacia afuera, el visitante sale de la página.
- **Nivel gratuito de Formspree (registro de un clic, el formulario se queda en la página).** Se registran gratis, obtienen una URL de endpoint del formulario que se ve como `https://formspree.io/f/xxxxxxx`, y la pegan. El formulario se envía sin salir de la página y los emails llegan a su bandeja de entrada. El nivel gratuito cubre unos 50 envíos al mes, que alcanza de sobra para averiguar si una idea tiene futuro. Desventaja: un registro.
- **`mailto:` simple (nada que configurar, la más débil).** El botón abre la app de email del visitante con un mensaje prellenado. Sin registro, sin cuenta, funciona al instante. Desventaja: mucha gente no lo va a terminar, así que trata el conteo como un piso, no como un número real.

Si no quieren decidir ahora mismo, constrúyela con la versión `mailto:` y deja un espacio de una línea claramente comentado arriba del código del formulario donde se pega después una URL de Formspree o Google Form. Diles la línea exacta para cambiar.

Sea cual sea la que elijan, la página también guarda cada email enviado en `localStorage` como respaldo, para que nada se pierda mientras están probando.

### 3. Escribe las cinco piezas de texto
Una página de lista de espera tiene cinco piezas y nada más. Escribe las cinco con su voz según el perfil.

1. **La línea de la promesa.** La que eligieron. Este es el titular.
2. **Una oración aclaratoria debajo.** Dice para quién es y qué reemplaza. Una oración. No un párrafo.
3. **El único campo.** Email. Etiquétalo con claridad: "Email". Marcador de posición: `tu@ejemplo.com`. Nunca pidas nombre, empresa, teléfono ni "cuál es tu mayor desafío." Cada campo extra recorta registros, y ninguna de esas respuestas cambia lo que van a construir.
4. **El botón.** Dice qué pasa, no "Enviar". Bien: "Avísame cuando esté listo." "Ponme en la lista." Mal: "Registrarse." "Empezar."
5. **Qué pasa después, con honestidad.** Una línea corta justo debajo del botón. Algo como: "Te mando un solo email cuando esté listo — más o menos en marzo. Ningún otro email. Eso es todo." Esta línea sube los registros más que cualquier otra cosa de la página, porque el miedo real es que los llenen de spam.

Opcionalmente, un bloque corto de tres o cuatro líneas diciendo qué va a hacer la cosa — pero solo si la promesa realmente lo necesita. La mayoría no.

Nunca inventes números. Nada de "únete a otras 500 personas" a menos que 500 personas realmente se hayan unido. Un contador falso en una página con cuatro registros es la forma más rápida de perder a los cuatro.

### 4. Construye la página
Construye un archivo. Incluye cada una de estas cosas:

- Un solo `index.html` autocontenido. Sin herramientas de build, sin librerías JS externas, sin frameworks.
- Google Fonts es el único recurso externo. Una fuente display para la línea de la promesa, una fuente para todo lo demás.
- Paleta contenida: un acento más neutros. **Nunca** el degradado genérico de IA de morado a azul. Si existe `~/.claude/design.md`, léelo y usa esa paleta, combinación de fuentes y espaciado en su lugar.
- Mobile first. Constrúyela para un teléfono de 375px de ancho y deja que crezca. La línea de la promesa tiene que caber sin barra de desplazamiento horizontal. El campo de email y el botón ocupan todo el ancho en móvil y tienen al menos 48px de alto.
- **Totalmente legible y usable sin JavaScript.** El titular, la promesa y el formulario funcionan todos con los scripts desactivados. Si eligieron Formspree o Google Form, el `<form action=... method="post">` de HTML simple lo maneja sin ningún script. JavaScript solo agrega los detalles agradables encima.
- Anima solo con transforms y opacity. Como máximo una entrada tranquila en la línea de la promesa. Sin desenfoque animado, sin filtros de ruido, sin marquesinas que se desplazan solas, nada en bucle infinito.
- Texto real de marcador de posición — las oraciones reales del paso 3. Nunca lorem ipsum.
- Cualquier ícono es SVG en línea.
- Un trabajo, una página: un solo llamado a la acción, sin barra de navegación, sin links de pie de página, sin íconos de redes sociales que alejen a la gente. Cada link que no sea el botón cuesta registros.
- Después de un envío exitoso, cambia el formulario por una línea corta de agradecimiento en el mismo lugar — sin recargar la página, sin ventana emergente. Con JavaScript desactivado, la propia acción del formulario lo maneja.
- Incluye la etiqueta `<meta name="viewport" content="width=device-width, initial-scale=1">`.
- Fija un `<title>` real y una meta descripción de una línea, para que el link se vea bien cuando alguien lo mande por mensaje.

### 5. Ponla frente a un desconocido
Una página sin lanzar no prueba nada. Feo pero en línea le gana a bonito pero local. Diles:

- Abrir primero el archivo en su navegador y comprobarlo en una ventana con tamaño de teléfono.
- Para ponerla en línea gratis: arrastrar la carpeta al plan gratuito de Vercel, o subir la carpeta a un repo de GitHub y activar GitHub Pages. Ambas dan una URL real que pueden mandar por mensaje.
- Luego mandársela a cinco personas que de verdad tengan el problema. No cinco amigos. Cinco personas con el problema.
- Qué observar: ¿se registran sin hacer una pregunta aclaratoria? Si tienen que preguntar "espera, ¿qué es esto?", lo que hay que arreglar es la línea de la promesa, no el diseño.

Fija el umbral honesto en voz alta: si 20 de las personas correctas la ven y menos de 3 se registran, esa es una respuesta real y les ahorró tres meses. Reescribe la promesa y mándala de nuevo antes de escribir una línea del producto.

## Resultado — guárdalo

Escribe la página en `~/sites/<slug>-waitlist/index.html` donde `<slug>` es un nombre corto para la idea.

Escribe también `~/sites/<slug>-waitlist/notes.md` con: la línea de la promesa que eligieron y las dos que no, para quién es, dónde llegan los emails más la línea exacta para cambiar si más adelante lo modifican, la fecha honesta, las cinco personas a las que planean mandarla y la regla de decisión (cuántos registros significan construirlo).

Diles ambas rutas, y luego:

> "Abre `~/sites/<slug>-waitlist/index.html` en tu navegador. Si se ve bien, ponla en línea gratis y mándale el link a cinco personas que de verdad tengan este problema — hoy, no después de más ediciones."

## Ejemplo (entrada → salida)

**Entrada:** "Quiero construir una app que ayude a los peluqueros caninos a manejar sus citas. Lo he estado pensando durante meses. No estoy seguro de si alguien la necesita."

**Salida (guardada en `~/sites/groomer-waitlist/index.html`):**

- **Línea de la promesa:** "Deja de perder citas de peluquería en tus mensajes de texto."
- **Oración aclaratoria:** "Una página de reservas simple hecha para peluqueros caninos independientes. Los clientes eligen un horario, tú dejas de jugar al teléfono."
- **Campo:** un campo de email, etiquetado "Email."
- **Botón:** "Avísame cuando esté listo."
- **Qué pasa después:** "Te mando un solo email cuando esté en línea — apunto a marzo. Nada más, nunca."
- **Los emails llegan:** nivel gratuito de Formspree, endpoint pegado en el `action` del formulario. Copia de respaldo guardada en `localStorage`.
- **Aspecto:** fondo crema, texto casi negro, un acento verde oscuro solo en el botón. Titular en Fraunces sobre cuerpo en Inter. Botón a todo el ancho de 52px de alto en móvil. Funciona con JavaScript desactivado.
- `notes.md` registra la regla de decisión: "20 peluqueros la ven. Menos de 3 registros significa que la promesa está mal — reescribir y reenviar antes de construir nada."

## Notas / casos especiales
- El error de principiante que esto evita: tres meses construyendo algo que nadie pidió. La página toma una noche. Haz la página primero.
- Si insisten en recolectar un nombre, un teléfono o una pregunta de encuesta, resístete una vez: cada campo cuesta registros, y ninguna de esas respuestas cambia lo que van a construir. Si aun así lo quieren, agrega solo el nombre.
- Si no tienen una fecha honesta, escribe "Todavía no tengo una fecha — te mando un email en el momento en que la tenga." Honesto y vago le gana a un mes inventado.
- Si la línea de la promesa necesita más de una oración para explicarse, la idea todavía no está lo bastante clara. Pasa a **positioning-filter** antes de construir la página.
- Una vez que esté en línea, ejecuta **mobile-check** sobre ella — la mayoría de la gente a la que le manden el link la va a abrir en un teléfono.
