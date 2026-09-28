---
name: first-product
description: Convierte lo que ya sabes en una guía digital terminada que puedes vender, en una sola sentada. Te entrevista sobre tu ángulo y tus lecciones, escribe la guía completa como un archivo limpio que puedes convertir en PDF, y luego escribe el texto de la ficha de la tienda (título, pitch, precio, tres viñetas) y la lista corta de cosas que todavía tienes que hacer a mano. Úsalo cuando el usuario diga "ayúdame a hacer un producto digital", "convierte lo que sé en un ebook", "arma una guía que pueda vender", "hazme algo para poner en Gumroad", "quiero vender un PDF", "qué puedo vender" o "/first-product".
---

# First Product: una guía, escrita y lista para vender esta noche

La mayoría de la gente nunca vende nada porque está esperando construir la gran cosa. Un primer producto no tiene que ser grande. Tiene que ser una guía enfocada que le enseñe a una persona a conseguir un resultado, vendida a un precio bajo en una tienda en línea (una página simple que cobra y entrega tu archivo, como Gumroad o Stan Store).

Este skill escribe esa guía contigo. No un esquema, no un plan. Las 20 a 40 páginas reales, más el texto para la página del producto. Terminas la sentada siendo dueño de un producto real.

## Personalización
Este skill escribe con *tu* voz, sobre *tu* experiencia. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nicho, tu audiencia y el resultado que ayudas a conseguir, y yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes números, resultados ni afirmaciones que el usuario no te dio.

## Pasos

### 1. Consigue lo básico: tres cosas
Sácalas primero del perfil y pregunta solo por lo que falte:
1. **Qué sabes hacer.** La habilidad real, no un cargo.
2. **Para quién es.** Un tipo de persona, nombrado de forma específica.
3. **El resultado.** Qué cambia para ellos después de seguir tu método.

Si el mensaje inicial es escaso ("ayúdame a armar algo para vender") y el perfil no lo cubre, pide estas tres cosas antes que nada. No adivines la experiencia de nadie. Una suposición equivocada aquí hace que toda la guía esté equivocada.

### 2. La entrevista: cuatro preguntas, no más
Pregunta solo lo que todavía falte. Nunca conviertas esto en un formulario de diez preguntas. La velocidad es el punto.

1. **Tu ángulo.** ¿Qué hace distinta tu versión de esto? Un momento específico, un resultado, un error que cometiste. Esto se convierte en el gancho, y es la razón por la que alguien te compra a ti en lugar de buscar el tema gratis en Google.
2. **Tus lecciones.** De tres a cinco cosas que le enseñarías a alguien que empieza desde cero. Se convierten en los capítulos. Si no pueden nombrarlas, propón un conjunto según su nicho y confírmalo antes de escribir.
3. **Una muestra de escritura.** Un post, un email, la transcripción de un video, cualquier cosa que hayan escrito. Si pegan una, imítala. Si no, usa el Tono del perfil de marca, y usa siempre sus propias palabras para su propio nicho.
4. **El precio.** Si no lo saben, recomienda uno y da la razón en una línea. No les entregues un menú:
   - $9 a $27 para una guía enfocada en un tema
   - $27 a $47 si viene con plantillas, hojas de trabajo o archivos de referencia
   - $47 a $97 si reemplaza algo por lo que de otro modo pagarían cientos

Sobre la extensión: la mayoría de los primeros productos tienen de 20 a 40 páginas, unas 4,000 a 8,000 palabras. Por defecto, corto, salvo que digan otra cosa. Una guía que se termina y se lee le gana a una larga que no.

### 3. Confirma la lista de capítulos
Convierte las lecciones en una lista de capítulos y muéstrala como una lista numerada corta. Introducción, un capítulo por lección, capítulo de cierre.

Este es el único punto de control. Consigue un sí aquí, porque una estructura equivocada desperdicia toda la escritura. Limítate a la lista. Sin pitch, sin preámbulo.

### 4. Escribe la guía completa
Cada capítulo se construye alrededor de UN desbloqueo: algo que el lector puede hacer después de leerlo y que antes no podía. No una pila de información.

Por capítulo:
- Abre con la situación real en la que está el lector, no con una definición.
- Enseña el único desbloqueo de forma simple, con un ejemplo real. Usa la propia historia del usuario donde la tengas; si no, un escenario plausible de su nicho presentado como ejemplo ("digamos que estás intentando...").
- Da la acción exacta que hay que tomar, no solo la idea.
- Párrafos cortos. El espacio en blanco trabaja.

Reglas de voz para cada oración:
- Palabras de nivel de quinto a octavo grado. Si un término es necesario, explícalo con palabras simples la primera vez que aparece.
- Una idea por oración. Corta cualquier cosa que pase de unas 20 palabras. Registro conversacional, como se habla.
- Sin aperturas de relleno ("En el mundo de hoy", "Vamos a sumergirnos"). Sin rodeos ("podría", "quizás", "tal vez"). Di la cosa.
- No digas lo mismo de tres formas para llegar a un número de páginas. Si ya está dicho, sigue adelante.
- Sin frases ingeniosas que suenan inteligentes pero no le dicen al lector qué hacer.
- Nunca inventes una estadística, un resultado de cliente ni una afirmación que el usuario no te dio.

Antes de dar un capítulo por terminado, revísalo: ¿se podría resumir como "aquí hay algo de contexto sobre X"? Entonces no está terminado. Corta el contexto y ve al desbloqueo.

### 5. Dale formato para que se convierta a PDF limpio
Escribe la guía en un solo archivo Markdown con esta forma:

```markdown
# [Título de la guía]
### [Una línea que diga qué cambia para el lector]

*por [Nombre del autor]*

---

## Introducción
[El ángulo y la historia. Qué podrán hacer al terminar. Para quién es, en una oración.]

---

## Capítulo 1: [Lección]
[Situación, luego el desbloqueo, luego la acción exacta.]

---

## Capítulo 2: [Lección]

(repetir para cada lección, de tres a cinco en total)

---

## Ponerlo en práctica
[La única siguiente acción para tomar esta semana.]
```

Reglas de seguridad para impresión, porque los conversores gratuitos de Markdown a PDF se rompen con todo lo demás:
- H1 para el título, H3 para el subtítulo, H2 para los capítulos. Nada más profundo.
- Sin tablas. Usa prosa corta o una lista simple de viñetas para comparar cosas.
- Sin bloques de código. Se ven como feas cajas grises en un ebook.
- Listas de viñetas de un solo nivel. Las viñetas anidadas se desarman.
- Negritas con moderación, solo para enfatizar. Nunca pongas en negrita una oración completa.
- Un `---` entre secciones, lo que da a la mayoría de los conversores un salto de página limpio.
- Sin imágenes, sin HTML. Mantenlo simple para que se pegue en Notion o Google Docs sin romperse.

No intentes generar un PDF. El entregable es el archivo limpio. Dile al usuario claramente: pégalo en Notion, Google Docs o una herramienta gratuita de Markdown a PDF y expórtalo. Ese PDF es lo que se sube.

### 6. Escribe el texto de la ficha de la tienda
Este es el texto para la página del producto en sí. Escríbelo exactamente con esta forma:

```
TÍTULO: [corto, dice el beneficio, coincide con el título de la guía]

PITCH (3 a 5 oraciones): para quién es, qué cambia para ellos, por qué esta persona
en concreto puede enseñarlo (su ángulo real del paso 2) y qué lo hace distinto
del material gratis sobre el mismo tema.

PRECIO: $[X], porque [una línea ligada a lo que vale el resultado].

LO QUE PODRÁS HACER:
- [cosa concreta]
- [cosa concreta]
- [cosa concreta]
```

Mantén el pitch anclado en el resultado real. Nunca lo infles con números que el usuario no te dio.

### 7. La lista honesta de lo que falta
Este skill no puede tocar una tienda en línea ni una cuenta de pagos, así que siempre cierra diciendo exactamente qué falta. Nada de esto se puede automatizar desde un skill:

```
LO QUE HACES A MANO:
[ ] Crear una cuenta en una tienda en línea (Gumroad, Stan Store o Payhip, elige una)
[ ] Conectar una cuenta de pagos (normalmente Stripe) para poder cobrar
[ ] Convertir guide.md a PDF (pégalo en Notion o Docs, exporta como PDF)
[ ] Crear un producto nuevo en tu tienda y subir el PDF
[ ] Pegar el título, el pitch y las viñetas de listing.md
[ ] Fijar el precio
[ ] Publicar y mandarle el link a una persona real hoy
```

## Resultado: guárdalo
Crea `~/guides/<guide-slug>/` y escribe dos archivos:
- `guide.md`, la guía completa, segura para imprimir.
- `listing.md`, el texto de la ficha del paso 6 más la lista del paso 7.

Dile al usuario ambas rutas. Luego una siguiente acción: convertir `guide.md` a PDF, porque todo lo demás depende de que ese archivo exista.

## Ejemplo (entrada → salida)
**Entrada:** "Llevo seis años entrenando perros. Sobre todo perros reactivos. La gente viene conmigo después de haber probado con otros tres entrenadores. Lo que siempre termino enseñando es que están premiando el momento equivocado."

**Salida (lista de capítulos, confirmada antes de escribir):** Introducción, la clienta que había despedido a tres entrenadores antes de mí. 1. Por qué tu perro reacciona antes de que tú siquiera veas el detonante. 2. La ventana de dos segundos que lo decide todo. 3. Premiar la calma en lugar de premiar el silencio. 4. Pasear a un perro reactivo sin temerle al paseo. Luego Ponerlo en práctica.

**Salida (extracto de `~/guides/reactive-dog-reset/listing.md`):**
> TÍTULO: El reinicio del perro reactivo
>
> PITCH: Para dueños cuyo perro se abalanza, ladra o se congela en cada paseo, y que ya probaron los consejos de siempre. Esta es la versión de seis años de lo que les enseño a los clientes que llegan a mí después de otros entrenadores. Aprenderás a detectar el momento antes de la reacción, y qué premiar en su lugar. Es específico para perros reactivos, no obediencia general.
>
> PRECIO: $27, porque una sesión presencial cuesta más que esto y cubre menos.

## Notas / casos especiales
- Si quieren un curso, una serie o un libro entero, díselo claramente y tráelos de vuelta aquí. Una guía terminada le gana a un curso que nadie lanza nunca.
- Si no pueden nombrar sus lecciones, es normal. Propón de tres a cinco a partir de lo que te dijeron en el paso 1 y deja que te corrijan. A la gente le resulta más fácil editar que inventar.
- Si todavía no tienen pruebas ni resultados, no inventes ninguno. El ángulo sostiene la guía. Un método específico bien enseñado vale la pena pagarlo sin un testimonio adjunto.
- Si la pregunta del precio los frena, elige el extremo bajo y sigue adelante. Pueden subirlo después de las primeras diez ventas.
- Si tienen una siguiente oferta hacia la que dirigir a los lectores, pregunta antes de agregar una mención al final. Nunca la agregues sin preguntar.
- La lista de capítulos es el único punto de control. Una vez confirmada, escribe todo de una vez. Detenerse a revisar cada capítulo es como un producto de una sentada se convierte en un proyecto de tres semanas.
