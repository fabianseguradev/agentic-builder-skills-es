---
name: make-it-designed
description: Toma una página que ya construiste y haz que se vea diseñada en lugar de por defecto, sin reconstruirla. Aplica una lista fija de pulido — una fuente display y una fuente para el cuerpo con saltos de tamaño seguros, una escala de espaciado real, una paleta contenida, una jerarquía que sobrevive a la prueba de entrecerrar los ojos — y luego agrega exactamente un toque distintivo para que la página tenga un punto de vista. Úsalo cuando el usuario diga "haz que esto se vea mejor", "funciona pero se ve mal", "haz que se vea diseñado", "pule esta página", "por qué mi sitio se ve barato", "parece una plantilla", "límpialo visualmente", "haz que se vea caro" o escriba /make-it-designed.
---

# Make It Designed — refina, no reconstruyas

Construiste algo y funciona, pero parece un formulario. El instinto es agregar: más colores, más secciones, más íconos, un video de portada. Ese instinto está mal. Las páginas diseñadas se ven diseñadas porque alguien quitó cosas hasta que solo quedaron las partes que funcionan, y luego agregó un detalle deliberado. Esto hace esa pasada sobre una página que ya tienes, y nunca la reconstruye desde cero.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Encuentra la página y fija la regla
Pide la ruta del archivo de la página. Si no la saben, busca `index.html` en las carpetas en las que han estado trabajando y confírmalo con ellos antes de tocar nada.

Luego lee todo el archivo y di la regla en voz alta, porque cambia lo que pasa después:

> "Voy a refinar esto, no a reconstruirlo. Tu contenido, tu estructura y tus links se quedan exactamente donde están. Solo voy a cambiar cómo se ve."

Antes de editar, diles: "Si odias el resultado, escribe `/rewind` y vuelve atrás. No puedes romper esto."

Si existe `~/.claude/design.md`, léelo y usa esa paleta, combinación de fuentes, escala y espaciado en lugar de inventar nuevos. Si no existe, menciona una vez que **design-taste** fijaría esas decisiones de forma permanente, y luego sigue con opciones razonables por ahora.

### 2. Quita tres cosas antes de agregar una
Recorre la página y encuentra al menos tres cosas para borrar. Esto no es opcional y pasa antes de cualquier agregado. Busca:

- **Colores más allá del tercero.** Cuenta cada color distinto de la página. Si hay más de cinco incluyendo el negro y el blanco, recorta a cinco.
- **Un segundo color de acento.** Hay un solo acento. El otro es decoración haciéndose pasar por significado.
- **Sombras paralelas que no hacen nada.** Una sombra debería decir "esto flota por encima de aquello". Si todo tiene sombra, nada flota. Borra la mayoría.
- **Bordes que duplican el espaciado.** Si un borde y un espacio grande separan dos secciones, quédate con el espacio y quita el borde.
- **Íconos que repiten las palabras de al lado.** Una marca de verificación junto a la palabra "incluido" no aporta nada.
- **Llamados a la acción repetidos.** Una página, un trabajo. Si hay tres botones distintos pidiendo tres cosas distintas, elige uno y convierte los otros en links de texto simples.
- **Párrafos de cuerpo centrados.** Los titulares centrados pueden funcionar. Los párrafos centrados son difíciles de leer. Alinea a la izquierda todo lo que pase de dos líneas.
- **Degradados que no hacen ningún trabajo,** empezando por el de morado a azul.

Muéstrales la lista de lo que recortaste y por qué, en una línea cada cosa.

### 3. Aplica la lista
Ahora arregla las cuatro cosas que marcan la diferencia. Trabaja en este orden.

**Tipografía — dos fuentes, saltos seguros.**
- Exactamente una fuente display para los titulares y una fuente para todo lo demás. Ambas de Google Fonts. Borra cualquier tercera fuente.
- Define seis tamaños sobre una proporción y usa solo esos. El error de principiante más común son los saltos tímidos: un titular de `1.5rem` sobre un cuerpo de `1rem` se lee como un accidente. Lleva el titular más grande a por lo menos 2.5 veces el tamaño del cuerpo. En un teléfono, por lo menos 2 veces.
- Texto del cuerpo entre 16px y 18px. Interlineado de 1.5-1.65 en el cuerpo, de 1.05-1.2 en los titulares grandes. Los titulares se ajustan más a medida que crecen — ese solo cambio hace más que cualquier elección de color.
- Largo de línea limitado a unos 65-75 caracteres (`max-width: 65ch`). Los párrafos a todo el ancho son la forma más rápida de verse sin terminar.

**Espaciado — una escala real, no conjeturas.**
- Elige una base de 8px y usa solo 8 / 16 / 24 / 40 / 64 / 96. Reemplaza cada número raro de la página (13px, 22px, 35px) por el paso más cercano.
- El espacio entre secciones debería ser mucho mayor que el espacio dentro de ellas. Si un encabezado está igual de lejos de su propio párrafo que de la sección de arriba, la página se lee como una sola masa. Más o menos: los espacios dentro de un grupo llevan un paso, los espacios entre grupos llevan tres pasos.
- Margen exterior generoso en móvil — 20-24px como mínimo, nunca texto tocando el borde de la pantalla.

**Paleta — contenida.**
- Cinco colores: texto, fondo, superficie, un acento, un gris apagado. Esa es toda la página.
- El acento aparece en menos del 10% de los píxeles. Marca la única cosa en la que quieres que hagan clic. Si el acento está en el encabezado, en tres titulares y en el pie, deja de significar algo.
- Comprueba el contraste real. Texto gris sobre fondo gris es la segunda señal más común de principiante.

**Jerarquía — la prueba de entrecerrar los ojos.**
- Entrecierra los ojos frente a la página (o desenfócala en tu cabeza) hasta que las palabras se vuelvan formas. Aun así deberías poder distinguir, en orden: qué es esto, qué hace por mí, dónde hacer clic.
- Si todo tiene el mismo peso y tamaño, nada va primero. Arréglalo con tamaño y peso, no con color.
- Exactamente una cosa en la pantalla debería ser la más llamativa. Normalmente el titular. A veces el botón. Nunca ambos.

### 4. Agrega exactamente UN toque distintivo
Ahora, y solo ahora, agrega una cosa. Una. Es lo que hace que la página se sienta hecha por una persona. Elige la que mejor encaje con la página y diles por qué la elegiste:

- **Un subrayado SVG dibujado a mano que se dibuja una vez.** Un trazo SVG en línea debajo de tres o cuatro palabras del titular, en el color de acento, con una forma ligeramente temblorosa, dibujada a mano — no una línea recta. Anímalo con `stroke-dasharray` / `stroke-dashoffset` para que se dibuje solo una vez al cargar, en unos 700ms, y luego se detenga. Nunca debe repetirse en bucle. Con JavaScript desactivado, el subrayado simplemente está ahí, ya dibujado.
- **Un tratamiento editorial del titular.** Tipografía display de gran tamaño, una palabra o frase en un estilo que contraste (serif en cursiva dentro de un titular sans, o el color de acento solo en dos palabras), ajustado, con una línea corta de antetítulo encima en versalitas o monoespaciada. Portada de revista, no landing page.
- **Una franja de datos "en números".** Una sola fila horizontal de tres números reales con etiquetas cortas debajo, sobre el color de superficie, con espacio generoso arriba y abajo. Solo números reales que el usuario realmente te dio. Si no tienen números, no inventes ninguno — elige otro toque distintivo.

Reglas para el toque: aparece una vez en la página, usa el acento y es lo único en la página que hace algo inesperado. Dos toques distintivos se anulan entre sí.

Cualquier movimiento es solo con transforms y opacity. Sin desenfoque animado, sin filtros de ruido, sin marquesinas que se desplazan solas.

### 5. Mantén la página honesta
Antes de terminar, verifica todo esto en el archivo editado:

- Sigue siendo un solo `index.html` autocontenido. No se agregaron herramientas de build ni librerías JS externas.
- Google Fonts es el único recurso externo.
- La página es totalmente legible con JavaScript desactivado. El toque distintivo se degrada a una versión estática.
- Mobile first: compruébala a 375px de ancho. El titular sigue cabiendo, nada se desplaza hacia los lados, el botón sigue siendo fácil de tocar.
- Texto real en todas partes. Si agregaste algún texto, dice algo verdadero sobre lo suyo. Nunca lorem ipsum.
- Los íconos son SVG en línea.

### 6. Muestra el antes y el después
Diles qué cambió en palabras simples — los recortes, los cuatro arreglos de la lista y el único toque distintivo. Luego diles que abran la página y te den una reacción en lenguaje simple. Haz una ronda de cambios a partir de esa reacción y detente.

## Resultado — guárdalo

Edita la página en su lugar, en su ruta original. Luego escribe un registro de cambios corto en `~/design-notes/<page-name>-polish.md` que contenga: qué quitaste y por qué, la combinación final de fuentes con sus tamaños, la escala de espaciado, los cinco códigos hex, qué toque distintivo agregaste y una línea sobre qué arreglar después si quieren seguir.

Diles ambas rutas, y luego:

> "Abre la página y actualízala. Si algo se ve mal, describe lo que ves en una oración — no toques el código."

## Ejemplo (entrada → salida)

**Entrada:** "Construí una landing page para mi negocio de paseo de perros. Funciona pero parece un formulario hecho en 2009. El archivo está en ~/dogwalk/index.html."

**Salida:**
- **Quitado:** el segundo azul, las sombras paralelas de las seis tarjetas, un borde que duplicaba un espacio de 64px, íconos de verificación que repetían las palabras de al lado y un botón "Saber más" que competía con "Reserva un paseo".
- **Tipografía:** DM Serif Display para los titulares, Inter para el cuerpo. Titular de `3rem` sobre cuerpo de `1.0625rem` — antes era `1.5rem` sobre `1rem`, y por eso se leía plano. Interlineado de 1.1 en el titular, 1.6 en el cuerpo, párrafos limitados a 65ch.
- **Espaciado:** todo ajustado a 8 / 16 / 24 / 40 / 64 / 96. Los espacios entre secciones pasaron de 30px a 96px. Ese solo cambio hizo la mayor parte del trabajo.
- **Paleta:** ink `#1A1A17`, paper `#FBF8F1`, surface `#FFFFFF`, accent `#2F6B4F`, muted `#77756D`. Ahora el acento aparece solo en el botón "Reserva un paseo" y en el subrayado del titular.
- **Toque distintivo:** un subrayado verde dibujado a mano debajo de "la hora favorita de tu perro", dibujado con un trazo SVG en línea en 700ms al cargar. No se repite. Queda ahí, estático, con JavaScript desactivado.
- Registro de cambios en `~/design-notes/dogwalk-polish.md`.

## Notas / casos especiales
- El error de principiante que esto evita: agregar más cosas para arreglar una página que se ve mal. Más cosas casi siempre son la causa. Quitar es el arreglo.
- Si la página está realmente rota — falta contenido, el diseño se desarmó — este no es el skill correcto. Dilo y arregla primero la estructura, luego vuelve.
- Si el usuario pide tres toques distintivos, di que no una vez y explica: el toque funciona porque es la única sorpresa. Tres sorpresas son ruido.
- Si el contenido en sí es el problema (sin una promesa clara, sin una acción clara), el diseño no lo va a salvar. Señálalo claramente — ninguna cantidad de espaciado arregla una página que no dice lo que hace.
- Ejecuta **mobile-check** después para detectar cualquier cosa que se rompa en un teléfono, y **design-taste** antes si quieren dejar estas decisiones fijadas en un archivo para cada proyecto futuro.
