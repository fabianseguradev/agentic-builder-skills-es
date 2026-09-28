---
name: positioning-filter
description: Encuentra y fija el ÚNICO ángulo que hace que tu oferta y tu contenido destaquen, para que dejes de sonar como todos los demás en tu nicho. Aplica un filtro de 3 preguntas (cuál es mi ángulo único, por qué le importaría a mi audiencia, cómo lleva a mi oferta) más una prueba de "qué recortar", y guarda una declaración de posicionamiento reutilizable + un diferenciador de una línea. Úsalo cuando el usuario diga "ayúdame a destacar", "cuál es mi ángulo", "por qué alguien me elegiría a mí", "sueno como todos los demás", "encuentra mi posicionamiento", "afila mi mensaje", o cuando su contenido o su oferta se sientan genéricos. Insiste en ejecutarlo antes de escribir contenido o una página de ventas.
---

# Positioning Filter — fija tu ángulo

La mayoría de la gente no fracasa porque su oferta sea mala, sino porque no se distingue. Este skill fuerza un ángulo único y defendible a través de tres preguntas y una prueba de recorte, y luego guarda una declaración de posicionamiento y un diferenciador de una línea que el usuario puede reutilizar en su bio, su contenido y su pitch.

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia — yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## Pasos

### 1. Pregunta 1 — ¿Cuál es mi ángulo único?
Toma del perfil el Qué haces, la Audiencia y la Prueba del usuario, y luego pídele que complete estas frases hasta que una se sienta afilada y verdadera:
- "Todos en mi nicho dicen ___. Yo digo ___ en cambio."
- "Lo que yo hago distinto es ___."
- "Mi ventaja injusta / mi trayectoria rara es ___." (su trabajo anterior, su propia transformación, un método que usa, una audiencia específica que entiende a fondo).
Insiste en un *contraste* — un ángulo solo se gana la atención cuando empuja contra el consejo por defecto. Anota el candidato más fuerte.

### 2. Pregunta 2 — ¿Por qué le importaría a mi audiencia?
Un ángulo solo es posicionamiento si la audiencia lo siente. Traduce el ángulo al lenguaje de la audiencia usando el Dolor principal del perfil:
- "Para [audiencia] que está cansada de [el enfoque común], yo [ángulo] para que puedan [resultado]."
- Ponlo a prueba: ¿toca un dolor que dirían en voz alta? Si es ingenioso pero no asentirían, es un eslogan, no posicionamiento. Reescríbelo hasta que caiga sobre un dolor real.

### 3. Pregunta 3 — ¿Cómo lleva a mi oferta?
El ángulo tiene que apuntar a lo que venden, o es solo personalidad. Conéctalos:
- "Mi ángulo lleva naturalmente a alguien a querer [oferta] porque ___."
- Si el ángulo atrae a una audiencia que nunca compraría la oferta, es el ángulo equivocado — señálalo y ajústalo.

### 4. La prueba de "qué recortar"
El posicionamiento se define tanto por lo que te niegas a ser. Aplica estos recortes:
- **Recorta la audiencia:** ¿para quién NO es esto, de forma explícita? Nómbralos. Repeler a la gente equivocada afila la atracción sobre la correcta.
- **Recorta los temas:** enumera 2–3 cosas del nicho de las que el usuario deliberadamente NO va a hablar, para que sea dueño de un carril en lugar de cubrirlo todo.
- **Recorta las coberturas:** quita el "también hago X, e Y, y Z". Una punta de lanza le gana a cinco.
Anota lo que se recortó — es la prueba de que el posicionamiento es específico.

### 5. Arma la declaración de posicionamiento + la frase de una línea
Escribe una declaración de posicionamiento corta con esta forma:
> "Ayudo a [audiencia específica] a [lograr un resultado] mediante [ángulo/método único], sin [lo que temen]. A diferencia de [lo habitual en el nicho], yo [diferenciador]."

Luego comprímela en una sola **línea diferenciadora** reutilizable para su bio/gancho, p. ej. "El tipo de [resultado] para [audiencia] que odia [el enfoque común]." Mantén ambas en el tono del usuario y con sus palabras prohibidas/favoritas.

## Resultado — guárdalo
Escribe el resultado en `~/offers/positioning.md` (crea `~/offers/` si hace falta). Incluye: el ángulo elegido, la línea de "por qué les importa" dirigida a la audiencia, el vínculo con la oferta, la lista de recortes (para quién/qué NO es), la declaración de posicionamiento completa y el diferenciador de una línea. Confirma la ruta y dile al usuario que puede pegar la frase de una línea en su bio y reutilizar la declaración en cualquier página de ventas.

## Ejemplo (entrada → salida)
**Entrada:** El usuario enseña a personas no técnicas a construir software con herramientas de IA. El nicho está inundado de contenido de "aprende a programar" y "trucos de IA".

**Salida (guardada en `~/offers/positioning.md`):**
- **Ángulo:** "Todos dicen que aprendas a programar. Yo digo que no hace falta — necesitas construir una cosa real por la que la gente pague."
- **Por qué les importa:** "Para quienes están cambiando de carrera y están cansados de tutoriales que no llevan a ningún lado, te llevo a un producto que funciona y se puede vender, no a un certificado."
- **Lleva a la oferta:** apunta directamente al programa "construye tu primer producto de pago".
- **Recortes:** no es para desarrolladores profesionales; no cubrirá algoritmos, entrevistas en pizarra ni cuál es el mejor framework.
- **Declaración de posicionamiento:** "Ayudo a personas no técnicas que están cambiando de carrera a construir y vender su primer producto de software usando IA, sin aprender a programar por el camino difícil. A diferencia de los bootcamps de programación, yo optimizo para conseguir un cliente que paga, no un portafolio."
- **Frase de una línea:** "El tipo de 'sáltate el bootcamp, construye el producto' para creadores no técnicos."

## Notas / casos especiales
- Si el usuario da tres ángulos distintos, haz que elija UNO para fijarlo ahora; puede probar los otros después. El posicionamiento difuso es el error a evitar.
- Generaliza a partir de la propia historia y la audiencia del usuario — nunca tomes prestado por completo el ángulo de otro creador.
- Si el ángulo no lleva a ninguna oferta que tengan, es una señal para arreglar la oferta (pasa a **offer-builder**) o el ángulo, no para lanzarlo tal cual.
