---
name: landing-page
description: Construye un sitio de una página con un solo trabajo — capturar un email o una reserva — con un titular, tres pruebas, un formulario, un botón y unas preguntas frecuentes que eliminan la objeción más grande. Incluye una configuración de formulario gratuita que funciona para que los emails realmente te lleguen. Úsalo cuando el usuario diga "constrúyeme una landing page", "/landing-page", "necesito una página para capturar emails", "página de suscripción", "una página para mi guía gratuita", "página de lista de espera", "página de lead magnet", "página de registro", "quiero que la gente me dé su email", "una página para mi newsletter" o "un lugar al que mandar a la gente desde Instagram".
---

# Landing Page — una página, un trabajo, un botón

La mayoría de las páginas de principiantes piden demasiado. Sígueme, y compra esto, y lee mi blog, y únete a la lista. Una página que pide dos cosas no consigue ninguna. Esto construye una página cuyo único trabajo es capturar un lead, con un formulario que de verdad llega a tu bandeja de entrada, guardada como un solo archivo que puedes poner en línea en minutos.

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia — yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## Pasos

### 1. Nombra el único trabajo en voz alta
Pregunta: "Cuando alguien sale de esta página, ¿qué es lo único que hizo?" Insiste hasta que sea una sola acción:
- Me dio su email para la guía gratuita.
- Agendó una llamada.
- Se unió a la lista de espera.

Luego di la regla claramente: **un trabajo por página.** Todo lo que no sirve a ese trabajo se quita. Sin barra de navegación, sin íconos de redes sociales, sin "mira mis otras cosas", sin un segundo botón que va a otro lado. Si se resisten, pregunta a cuál renunciarían si solo pudieran quedarse con uno — ese es el trabajo.

Reúne también, del perfil o preguntando:
- **Para quién es**, con palabras específicas (no "emprendedores" — "gente que renunció a su trabajo el mes pasado y todavía no tiene clientes").
- **El único resultado** que obtienen. Qué cambia en su vida después.
- **Tres pruebas** — reales. Cosas que han hecho, resultados que pueden nombrar o datos concretos sobre lo que hay adentro. Si todavía no tienen pruebas, usa en su lugar tres detalles concretos sobre la cosa en sí. Nunca inventes un testimonio ni un número.
- **La objeción principal.** La razón por la que alguien lee esto y cierra la pestaña. Normalmente: ¿de verdad es gratis?, ¿cuánto tiempo toma?, ¿me vas a llenar de spam?, ¿es para alguien de mi nivel?

### 2. Escribe el texto antes de construir nada
Completa exactamente este esqueleto con su voz. Oraciones cortas. Concreto, no ingenioso.

- **Titular** — promete UN resultado. No lo que es, lo que obtienen. "Consigue tu primer cliente que paga en 30 días" le gana a "El Sistema de Adquisición de Clientes".
- **Subtítulo** — nombra para quién es y qué es la cosa. "Una guía gratuita de 12 páginas para freelancers que nunca han vendido nada."
- **Tres pruebas** — una línea cada una, fáciles de escanear, sin párrafos.
- **El formulario** — con la menor cantidad de campos posible. Solo email, salvo que de verdad necesiten un nombre. Cada campo extra cuesta registros.
- **El botón** — dice qué pasa después, en primera persona o con un verbo simple. "Envíame la guía." No "Enviar".
- **Bloque de preguntas frecuentes** — tres o cuatro preguntas como máximo, y la primera elimina de frente la objeción principal.
- **Una línea debajo del botón** que les dice qué pasa después: "Te llega a tu bandeja de entrada en más o menos un minuto. Sin spam, date de baja cuando quieras."

Relee el texto y corta todo lo que no empuje hacia el único trabajo.

### 3. Configura adónde van los emails
El formulario tiene que entregar en algún lado de verdad o la página es decoración. Dales estas dos opciones, en una frase cada una, y deja que elijan:

- **Formspree (recomendado)** — gratis, sin código: regístrate en formspree.io, crea un formulario, pega la URL que te da en el `action` del formulario y recibes los envíos por email. Pídeles la URL y conéctala.
- **Alternativa con mailto** — sin registro: el botón abre la app de email del visitante con un mensaje prellenado dirigido a tu dirección. Es más feo y menos gente lo completa, pero funciona ya mismo sin nada que configurar.

Si no quieren detenerse a registrarse, construye con la alternativa mailto y deja en el archivo un comentario de una línea claramente marcado donde irá la URL de Formspree más adelante. Nunca dejes un formulario que en silencio no llega a ningún lado.

### 4. Construye la página
Un solo `index.html` autocontenido:
- Sin herramientas de build, sin librerías de JavaScript externas. Google Fonts es el único recurso externo — una fuente display, una fuente para el cuerpo, elegidas para encajar con su marca.
- Un color de acento más neutros. Nunca el degradado de IA de morado a azul. El acento se usa para exactamente una cosa: el botón.
- Animación solo con transforms y opacity, usada con moderación. Sin desenfoque ni ruido animados, sin marquesinas que se desplazan solas.
- Totalmente legible y que se pueda enviar con JavaScript desactivado — un envío de formulario HTML simple, no un manejador en JS. Mobile first; asume un teléfono en una mano.
- El texto real del paso 2, nunca lorem ipsum. SVG en línea para cualquier ícono. Fotos solo si aportaron una o aprobaron una imagen gratuita de Unsplash.
- Orden de arriba a abajo: titular, subtítulo, formulario + botón, tres pruebas, segundo botón, preguntas frecuentes, pie de una línea. El formulario arriba en la página Y una repetición del botón después de las pruebas.

Guarda en `~/sites/<slug>/index.html`.

### 5. Previsualiza y luego haz el ciclo
Ábrelo:

```bash
open ~/sites/<slug>/index.html
```

Pregunta: "Léelo como un desconocido en su teléfono. ¿Qué es lo primero que te hace dudar?" Arregla una cosa a la vez en lenguaje simple. De cinco a diez rondas es lo normal.

Haz esta revisión cada un par de rondas y dila en voz alta: **¿hay algo en esta página que compita con el único trabajo?** Si lo hay, quítalo.

Luego prueba el formulario una vez de verdad — que lo envíen ellos mismos y confirmen que el email llega. Una página que se ve perfecta y se traga los leads es peor que una fea que funciona.

### 6. Guarda el archivo de notas y pasa el relevo
Escribe `~/sites/<slug>/NOTES.md` con el único trabajo, el titular, adónde entrega el formulario y el siguiente paso en una línea.

Cierra con: "Ejecuta **deploy-it** para tener esto en un link real, y luego pon ese link hoy en un lugar donde la gente ya te ve."

## Resultado — guárdalo
- `~/sites/<slug>/index.html` — la landing page, un archivo, formulario funcionando.
- `~/sites/<slug>/NOTES.md` — el único trabajo, el titular, el destino del formulario y el siguiente paso de mañana.

Indica ambas rutas. Única siguiente acción: ejecutar **deploy-it** y luego pegar el link en su bio o enviarlo a su lista.

## Ejemplo (entrada → salida)
**Entrada:** "Hice una checklist gratuita para gente que deja su trabajo para hacerse freelance. Quiero una página donde puedan conseguirla."

**Salida (guardada en `~/sites/freelance-checklist/index.html`):**

- **Titular:** "Sabe exactamente qué dejar listo antes de renunciar."
- **Subtítulo:** "Una checklist gratuita de 2 páginas para gente que deja un sueldo para ser freelance en los próximos 90 días."
- **Formulario:** un campo de email. Botón: **"Envíame la checklist."** Debajo: "Llega en más o menos un minuto. Sin spam, date de baja cuando quieras."
- **Prueba:** *Escrita a partir de 4 años de hacerlo mal primero* / *Cubre impuestos, margen de ahorros y tus primeros tres clientes* / *Dos páginas, no un ebook de 40*
- **Preguntas frecuentes:** "¿De verdad es gratis?" — "Sí. Sin tarjeta, sin llamada, sin cadena de emails de venta adicional." Más otras dos.
- El formulario envía a su URL de Formspree. Nada más en la página — sin navegación, sin links a redes, sin segunda oferta.

## Notas / casos especiales
- El error que esto evita: una página con cinco links donde el visitante no elige ninguno. Si el usuario insiste en agregar un segundo llamado a la acción, pregunta cuál borraría si se viera obligado. Esa respuesta es la página.
- Si todavía no tienen pruebas, usa datos concretos sobre la cosa (extensión, formato, qué cubre) en lugar de resultados. Nunca escribas un testimonio que no recibieron.
- Si no pueden nombrar la objeción principal, pregunta qué diría un amigo si se la mandaran ahora mismo. Normalmente es eso.
- Si la URL del formulario no está configurada, dilo en voz alta al final — no dejes que lancen una página que pierde en silencio cada registro.
- Derivación: **deploy-it** para publicar. **offer-builder** si lo que están regalando no está claro. **sales-page** si en realidad intentan vender, no capturar. **hooks** si el titular sigue saliendo plano.
