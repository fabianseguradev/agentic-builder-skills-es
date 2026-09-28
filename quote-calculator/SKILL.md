---
name: quote-calculator
description: Construye un pequeño widget de cotización instantánea para un negocio de servicios — el comprador elige algunas opciones y ve un rango de precio al instante, y luego deja sus datos de contacto. Sirve para mudanzas, limpieza, jardinería, pintores, retiro de escombros, lavado de autos a detalle, reparaciones del hogar. Un solo archivo HTML autocontenido, sin backend, nada que pagar, y es una de las cosas más fáciles que un principiante puede construir para un negocio local y cobrar por ello. Úsalo cuando el usuario diga "construye una calculadora de cotizaciones", "herramienta de cotización instantánea", "estimador de precios para mi sitio web", "que los clientes vean un precio", "calculadora de precios", "herramienta de estimación para mi negocio de limpieza", "algo que pueda venderle a negocios locales" o escriba /quote-calculator.
---

# Quote Calculator — un rango de precio en diez segundos, y un lead al final

Los negocios de servicios pierden la mayoría de sus leads en el mismo lugar: alguien quiere saber más o menos cuánto cuesta, el sitio dice "llame para cotizar" y termina llamando a otro. Una calculadora pequeña que da un rango honesto lo resuelve. También es una de las primeras cosas que un principiante puede construir por la que un negocio local real va a pagar, porque tapa un agujero que el dueño ya sabe que tiene.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Consigue el negocio y la lógica real de precios
Pregunta qué hace el negocio y para quién es. Luego consigue los precios, que son todo el trabajo. Pregunta exactamente esto:

> "Explícame cómo le pones precio realmente a un trabajo. ¿Cuál es el número de partida y qué hace que suba? Dame un trabajo real reciente y lo que cobraste por él."

Insiste hasta tener:
- **Una base.** Un mínimo, una tarifa por unidad o un precio de partida. Siempre hay uno, aunque el dueño nunca lo haya dicho en voz alta.
- **Las 3-5 cosas que mueven el precio.** No diez. Las cosas que realmente hacen variar el número. Para una mudanza: tamaño de la casa, distancia, escaleras o ascensor, ayuda con el embalaje. Para limpieza: dormitorios, baños, una sola vez vs recurrente, extras. Para un pintor: habitaciones, techos, estado de la preparación. Para retiro de escombros: cuánto cabe en el camión, escaleras, objetos pesados.
- **Cómo cambia el número cada una.** Un multiplicador ("2x para una casa de dos pisos"), un monto fijo ("+$150 por el embalaje") o una tarifa por unidad ("+$35 por habitación extra").
- **El piso y el techo.** El trabajo más pequeño que aceptarían y el más grande que cotizarían sin verlo en persona.

Si no saben sus propios números, no inventes ninguno. Guíalos por tres trabajos reales anteriores y aplica ingeniería inversa al patrón con ellos. Nunca inventes precios para un negocio real.

### 2. Diseña el rango, no el número
Esta es la regla que los mantiene fuera de problemas: **muestra siempre un rango, nunca un único número fijo.**

Un solo número es una promesa. Cuando el equipo llega y el trabajo es peor de lo descrito, el cliente les exige el número y alguien absorbe la diferencia o el trato se cae. Un rango fija una expectativa y mantiene abierta la conversación.

- Arma el rango como más o menos ±15-20% alrededor del punto medio calculado, y redondea a números limpios. `$340-$410`, no `$347.83-$412.19`.
- Amplía el rango cuando las respuestas son más vagas. Una respuesta de "casa grande, muchas cosas" merece un margen más amplio que "3 dormitorios, 1,400 pies cuadrados".
- Muestra el rango en grande — es la única razón por la que alguien tocó la página.
- Pon una línea honesta justo debajo, en letra más pequeña: "Esto es una estimación basada en lo que nos contaste. Tu precio final se confirma después de una llamada rápida o una foto." Esa oración es la red de seguridad legal y humana.
- Agrega debajo del rango un desglose en lenguaje simple que muestre qué lo determinó: "Base limpieza 3 dormitorios $180 · Limpieza profunda +$90 · 2 baños extra +$50." La gente confía en un número del que puede ver las partes.
- Si una respuesta pone el trabajo fuera de lo que cotizarían sin verlo, no muestres ningún rango. Muestra: "Este es lo bastante grande como para que una cotización real le gane a una suposición — déjanos tus datos y te llamamos hoy."

### 3. Captura el lead al final, y solo al final
El rango es lo que vinieron a buscar. El formulario de contacto es lo que paga el negocio. El orden importa.

- Muestra el rango **primero**, sin pedir email. Bloquear el número es la razón por la que fallan la mayoría de estas herramientas — la gente se va antes que cambiar un email por una suposición.
- Justo debajo del rango, pon la captura: nombre, teléfono o email y un cuadro opcional para un detalle. Tres campos como máximo.
- El botón dice qué pasa después. "Asegurar esta cotización." "Mándame el número real." Nunca "Enviar".
- Una línea debajo del botón que fije expectativas: "Te llamamos dentro de un día hábil. Sin spam."
- Al enviar, muestra la confirmación en el mismo lugar — sin recargar, sin ventana emergente. Guarda además el envío completo en `localStorage` (todas sus respuestas más el rango calculado) para que el dueño tenga un respaldo y pueda verlo incluso antes de conectar un servicio de formularios.
- Adónde va realmente el lead, opciones gratuitas: un endpoint gratuito de **Formspree** pegado en el `action` del formulario (un registro, el formulario se queda en la página, unos 50 al mes gratis), un **Google Form** al que la página envía los datos (los emails caen en una hoja que ya es suya) o una alternativa simple con `mailto:` que abre su app de email. Construye con la alternativa `mailto:` y deja una línea claramente comentada arriba del formulario donde se pega el endpoint real. Diles la línea exacta a cambiar.

### 4. Construye el widget
Un archivo. Incluye cada una de estas cosas:

- Un solo `index.html` autocontenido. Sin herramientas de build, sin librerías JS externas, sin backend, sin base de datos. Todas las cuentas de precios están en JavaScript simple dentro del archivo.
- Google Fonts es el único recurso externo. Una fuente display para el precio, una fuente para todo lo demás.
- Paleta contenida: un acento más neutros. **Nunca** el degradado genérico de IA de morado a azul. Si existe `~/.claude/design.md`, léelo y usa esa paleta, combinación de fuentes y espaciado.
- Mobile first, porque la mayoría de la gente completa esto en un teléfono, parada en la habitación que quiere que le limpien. Campos de al menos 48px de alto, zonas táctiles grandes, una pregunta por fila en una pantalla angosta, sin scroll lateral a 375px de ancho.
- Usa los tipos de campo correctos para que los teléfonos muestren el teclado correcto: `type="tel"` para el teléfono, `type="email"` para el email, `type="number"` para cantidades.
- **Totalmente legible sin JavaScript.** Con los scripts desactivados, la página sigue mostrando qué hace el negocio, la lista de opciones, la tabla de rangos de precio o el precio de partida en texto simple y un formulario de contacto que funciona. El cálculo en vivo es la mejora, no la página.
- El rango se actualiza en el momento en que cambia una opción. Sin botón de "Calcular" — una cosa menos que tocar.
- Anima solo con transforms y opacity. El número del precio puede aparecer y deslizarse un poco cuando cambia. Sin desenfoque animado, sin filtros de ruido, sin marquesinas, nada en bucle.
- Texto real en todo, escrito para este negocio específico. Nunca lorem ipsum.
- Íconos en SVG en línea. Sin fuentes de íconos, sin archivos de imagen.
- Incluye la meta etiqueta viewport y un `<title>` real.
- Mantén cada precio y multiplicador en un bloque claramente etiquetado arriba del script, con un comentario encima: "Todos los precios viven aquí. Cambia estos números para cambiar cada cotización." El dueño va a querer subir los precios la próxima primavera sin llamar a nadie.
- Hazlo fácil de insertar: funciona como página independiente y también dentro de un `<iframe>` en un sitio existente. Menciona ambas opciones cuando lo entregues.

### 5. Compruébalo contra trabajos reales
Antes de darlo por terminado, pasa por la calculadora los tres trabajos reales del paso 1 y compara. Si la calculadora dice $290-$350 y en realidad cobraron $520, la que está mal es la lógica, no el cliente. Arregla los números y vuelve a probar.

Revisa también los extremos: la selección más pequeña posible, la más grande posible y todas las opciones al máximo a la vez. Si alguna de esas produce un número absurdo, limítalo o mándalo al mensaje de "hablemos".

### 6. Diles cómo usarlo
Dos caminos, menciona ambos:
- **Para su propio negocio:** abrir el archivo, revisarlo en un teléfono, luego ponerlo en línea gratis con el plan gratuito de Vercel o con GitHub Pages, y enlazarlo desde su sitio actual como "Obtén una estimación instantánea".
- **Para venderlo a un negocio local:** construir una para un negocio de su ciudad usando los precios públicos reales de ese negocio, mandársela al dueño como un link que funciona y decirle "Hice esto para ti, ¿lo quieres en tu sitio?". Algo que funciona le gana a un pitch. Es un primer trabajo pagado normal.

## Resultado — guárdalo

Escribe el widget en `~/sites/<business-slug>-quote/index.html`.

Escribe también `~/sites/<business-slug>-quote/pricing-notes.md` con: el precio base, cada opción y exactamente cómo mueve el número, el ancho del rango, el piso y el techo, los tres trabajos reales con los que probaste y lo que la calculadora devolvió para cada uno, adónde van los leads más la línea a cambiar, y una nota corta de "cómo cambiar tus precios" que apunte al bloque etiquetado del archivo.

Diles ambas rutas, y luego:

> "Abre `~/sites/<business-slug>-quote/index.html` y pasa un trabajo real por ella. Si el rango no coincide con lo que cobrarías de verdad, dime cuánto habrías cobrado y arreglo los números."

## Ejemplo (entrada → salida)

**Entrada:** "Mi amigo tiene una empresa de retiro de escombros. Nunca publica precios y dice que la gente llama, pregunta cuánto cuesta y cuelga. Cobra según cuánto cabe en el camión."

**Salida (guardada en `~/sites/haulaway-quote/index.html`):**

- **Opciones:** cuántas cosas (un cuarto de camión / medio camión / tres cuartos / camión completo), escaleras (ninguna / un tramo / dos o más), objetos pesados (ninguno / uno / dos o más) y servicio en el mismo día.
- **Lógica:** base según la fracción del camión — $150 / $290 / $410 / $540. Escaleras: +$40 por tramo. Objetos pesados: +$75 cada uno. Mismo día: +20%.
- **Rango:** punto medio ±15%, redondeado a $10. Medio camión, un tramo de escaleras y un objeto pesado muestra **$345-$465**.
- **Debajo del rango:** "Base carga de medio camión $290 · Un tramo de escaleras +$40 · Un objeto pesado +$75." Luego: "Esto es una estimación basada en lo que nos contaste. Tu precio final se confirma cuando vemos la carga."
- **Más de un camión completo:** sin rango. Muestra "Ese es un trabajo de dos viajes — déjanos tu número y te damos una cotización real hoy."
- **Captura:** nombre, teléfono (`type="tel"`), un campo opcional de "algo que debamos saber". El botón dice "Asegurar esta cotización." Se guarda en `localStorage` y se envía a un endpoint de Formspree.
- **Aspecto:** texto casi negro sobre color hueso, un acento naranja solo en el precio y el botón. El precio aparece y se desliza 4px cuando cambia. Funciona con JavaScript desactivado — en su lugar se muestra la tabla de precios simple.
- **Probado:** tres de sus trabajos anteriores dieron $310-$420 (cobró $380), $520-$700 (cobró $610) y $150-$210 (cobró $175). Lo bastante cerca como para lanzarlo.

## Notas / casos especiales
- El error de principiante que esto evita: construir un sitio grande de varias páginas para un negocio local cuando lo único que le hace ganar dinero al dueño es un precio en la página.
- Nunca inventes precios para un negocio real. Si el dueño no puede decir sus números, aplícales ingeniería inversa a partir de tres facturas reales anteriores con el dueño presente.
- Si quieren un único número exacto en lugar de un rango, di que no una vez y explica por qué: un número exacto es una promesa que el equipo tiene que cumplir sin haber visto el trabajo. Si aun así insisten, muestra un número y pon "desde" delante.
- Con más de cinco preguntas la gente abandona a la mitad. Si el dueño quiere nueve preguntas, dile que la versión de nueve preguntas consigue menos leads que la de cuatro, y deja las extra para la llamada de seguimiento.
- Ejecuta **mobile-check** sobre ella antes de que salga en línea — casi todo el mundo la va a usar en un teléfono. Usa **make-it-designed** si funciona pero parece una hoja de cálculo.
