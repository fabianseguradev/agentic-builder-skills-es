---
name: first-website
description: Construye tu primer sitio web real describiendo lo que quieres en lenguaje simple — sin código, sin configuración, un solo archivo que puedes abrir y ver. Te guía por el Ciclo de Construcción (describir, previsualizar, reaccionar, repetir) durante 5-10 rondas hasta que la página se vea bien, y luego lo pasa para ponerlo en línea. Úsalo cuando el usuario diga "constrúyeme un sitio web", "quiero hacer un sitio web", "/first-website", "hazme un sitio", "necesito una página para lo mío", "puedes construirme un sitio web", "nunca he construido un sitio web", "no sé programar pero quiero un sitio", "haz una página de inicio" o "construye mi primer sitio web".
---

# First Website — descríbelo, míralo, arréglalo, lánzalo

Nunca has construido un sitio web, y no vas a empezar aprendiendo a programar. Vas a describir lo que quieres, mirarlo, decir qué está mal en palabras normales y repetir hasta que quede bien. Ese ida y vuelta no es que estés fallando. ESE es el trabajo. Al final tienes un archivo real en tu computadora que se abre en un navegador y parece algo que le mostrarías a una persona.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Fija el marco antes de construir nada
Dile al usuario, en dos o tres oraciones cortas:
- No va a escribir ni leer código. Describe resultados; tú construyes.
- Vas a construir una primera versión rápido, a propósito, para que haya algo a lo que reaccionar. No va a quedar bien la primera vez. Está bien.
- No puede romper nada. Si un cambio lo empeora, escribe `/rewind` (o presiona Esc dos veces con el cuadro de texto vacío) y vuelve atrás.

Luego di: "Cuéntame sobre el sitio que quieres. Solo habla — yo te pregunto lo que necesite."

### 2. Pasa de vago a quirúrgico
Esto es todo el skill. Un brief vago produce una página genérica. Toma lo que haya dicho y llévalo a cuatro cosas concretas. Pregunta solo lo que falte, y pregunta en palabras simples — nunca más de tres preguntas a la vez.

- **El visitante.** ¿Quién llega aquí? No "todo el mundo". Alguien específico: una novia buscando fotógrafo, un reclutador comprobando que eres real, el amigo de un amigo que escuchó que arreglas bicicletas.
- **La única acción.** ¿Qué es lo único que quieres que hagan? Agendar una llamada. Escribirte un email. Leer tu trabajo. Comprar. Elige una. Si nombran dos, haz que las ordenen y quédate con la primera.
- **La sensación.** Tres palabras para cómo debería sentirse. Tranquilo y caro. Ruidoso y divertido. Silencioso y serio. Esto es lo que convierte una plantilla en su página.
- **Las restricciones.** ¿Qué tiene que estar sí o sí (nombre, foto, precios, una cita específica)? ¿Qué NO debe estar (nada de fotos de stock de apretones de manos, nada de pop-ups, nada de testimonios falsos)?

Muéstrales la diferencia en voz alta una vez, usando su propio tema:

> **Vago:** "Hazme un sitio web para mi negocio de paseo de perros."
> **Quirúrgico:** "Un sitio de una página para un negocio de paseo de perros en Oakland. El visitante es un dueño de perro que trabaja y se siente culpable de que su perro esté solo todo el día. La única acción es mandarme un mensaje para reservar un paseo. Debe sentirse cálido, local y confiable — no corporativo. Debe incluir: mi nombre, Maya, los barrios que cubro, $25 por paseo, mi número de teléfono. No debe incluir: fotos de stock, un formulario de contacto, nada sobre 'soluciones para el cuidado de mascotas'."

Di: "La segunda te da un sitio. La primera te da una plantilla. Todo lo que construyas conmigo funciona así."

### 3. Construye la versión uno
Escribe un solo `index.html` autocontenido. Incluye esto siempre:

- Un archivo. Todo en línea — sin herramientas de build, sin librerías de JavaScript externas, nada que instalar.
- Google Fonts es lo único externo que puedes cargar. Una fuente display para los títulos, una fuente para el cuerpo. Elige fuentes que coincidan con sus tres palabras de sensación.
- Un color de acento más neutros. Nunca el degradado de morado a azul que tiene toda página hecha con IA. Si sus palabras de sensación son cálidas, el acento es cálido.
- Animación solo con transform y opacity, y solo un poco. Sin desenfoque animado, sin ruido en movimiento, sin marquesinas que se desplazan solas.
- La página debe leerse bien con JavaScript desactivado. Constrúyela mobile first — la mayoría la va a abrir en un teléfono.
- Texto real escrito para su visitante real. Nunca lorem ipsum. Nunca datos, precios, reseñas ni credenciales inventados — si necesitas un número que no tienes, pregunta o deja un espacio en blanco claramente marcado.
- Íconos como SVG en línea. Fotos solo si te dieron una, o una URL gratuita de Unsplash que aprueben.

Estructúrala de forma simple: un titular que diga qué es esto y para quién, un párrafo corto, prueba o detalle, y la única acción como un solo botón obvio. Un botón. Repetido como máximo dos veces a lo largo de la página.

Guarda en `~/sites/<slug>/index.html` donde `<slug>` es un nombre corto en minúsculas de su proyecto (`maya-dog-walking`). Crea las carpetas.

### 4. Previsualízalo y dales la pregunta para reaccionar
Ábrelo para que lo vean:

```bash
open ~/sites/<slug>/index.html
```

(En Windows, en una terminal que lo soporte, diles que hagan doble clic en el archivo en su lugar.)

Luego pregunta exactamente esto: **"Míralo. ¿Qué es lo primero que te molesta?"**

No "¿qué te parece?". No "¿algún comentario?". Una molestia específica a la vez es lo que produce una buena página. Si dicen "no sé, está bien", insiste una vez: "¿Qué te impediría mandarle esto a alguien? Nombra una cosa."

### 5. Haz el ciclo, 5-10 rondas
Cada ronda: dicen una cosa en lenguaje simple, tú la cambias, vuelven a mirar. Nunca les pidas que toquen el archivo.

Enséñales a describir el síntoma, no el arreglo. "El titular es demasiado pequeño en mi teléfono" es una gran nota. "Cambia el h1 a 3rem" no es su trabajo.

Buenas notas para mostrarles como modelo si se traban:
- "Hay demasiado espacio arriba antes de ver algo."
- "El botón no parece que se pueda hacer clic."
- "Esto se siente como un folleto corporativo, lo quiero más amigable."
- "Las palabras son difíciles de leer sobre ese fondo."

Cada 2-3 rondas, di: "Este es un buen punto de control — ¿quieres que lo guarde como punto de control?" y, si dicen que sí, haz un guardado permanente con Git para que siempre puedan volver a esta versión exacta.

Detén el ciclo cuando se lo mandarían a una persona. No cuando esté perfecto. Lo perfecto no llega hoy.

### 6. Escribe el archivo de notas y pasa el relevo
Escribe `~/sites/<slug>/NOTES.md` con qué es el sitio, para quién es, la única acción, las palabras de sensación y una línea de "la próxima vez voy a..." para que los 90 minutos de mañana empiecen con una lectura y no con una mirada perdida.

Luego cierra con el relevo, con estas palabras:
"Ahora mismo esto solo existe en tu computadora. Ejecuta **deploy-it** y lo pongo en una dirección web real, gratis. Luego mándale ese link a un ser humano de verdad hoy — no para presumir, solo para haber lanzado algo. Feo pero en línea le gana a bonito pero guardado en una carpeta."

## Resultado — guárdalo
- `~/sites/<slug>/index.html` — el sitio funcionando, un archivo, se abre en cualquier navegador.
- `~/sites/<slug>/NOTES.md` — qué es, para quién es, la única acción, las tres palabras de sensación y el siguiente paso de mañana en una línea.

Dile al usuario ambas rutas en voz alta. Única siguiente acción: ejecutar **deploy-it**.

## Ejemplo (entrada → salida)
**Entrada:** "Quiero un sitio web para lo de paseo de perros. Paseo perros en Oakland. No sé bien qué debería tener."

**Salida (después de la pasada quirúrgica y 6 rondas, guardada en `~/sites/maya-dog-walking/index.html`):**

Un sitio de una página. Un titular grande y cálido: **"Tu perro no tiene por qué pasar todo el día solo."** Debajo: "Maya pasea perros en Rockridge, Temescal y Piedmont Ave. 30 minutos, $25, con foto cada vez." Tres bloques cortos: *El mismo paseador siempre* / *Una foto de cada paseo* / *Escríbeme antes de las 9am para un lugar el mismo día*. Un color de acento (un naranja óxido suave), una fuente display, una fuente para el cuerpo. Un solo botón grande que dice **Escríbele a Maya — (510) 555-0143** y nada más compitiendo con él.

`NOTES.md` termina con: "La próxima vez: agregar las dos fotos de Rocco y Juno de mi teléfono."

## Notas / casos especiales
- El error que esto evita: un principiante que pide "un sitio web", recibe una plantilla genérica, no siente nada y abandona. La pasada quirúrgica del paso 2 no es opcional — hazla aunque estén impacientes.
- Si solo te dan una línea y no responden preguntas, construye algo de todos modos y deja que reaccionen. Reaccionar es más fácil que escribir un brief, y una mala versión le gana a una página vacía.
- Si piden un login, una base de datos, pagos o un blog con muchos posts, diles claramente que eso es un proyecto más grande y que el trabajo de hoy es una página que funcione. Anótalo en `NOTES.md` como un paso posterior.
- Nunca inventes precios, testimonios, nombres de clientes ni resultados. Si una sección necesita un número que no tienen, deja un espacio marcado y diles qué completar.
- Derivación: **deploy-it** para ponerlo en línea. **landing-page** si el trabajo real es capturar emails, no presentarse. **link-in-bio** si en realidad solo necesitaban una lista de botones para redes sociales.
