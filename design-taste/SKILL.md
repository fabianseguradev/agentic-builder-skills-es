---
name: design-taste
description: Convierte "no tengo buen gusto" en un sistema de diseño escrito que es tuyo. Nombras o haces captura de 1-3 sitios que te encantan, y esto aplica ingeniería inversa a los colores exactos, la combinación de fuentes, el ritmo de espaciado y las reglas que hay debajo, y luego guarda un archivo de diseño que lee cada proyecto futuro para que lo tuyo deje de parecer una plantilla por defecto. Úsalo cuando el usuario diga "no tengo buen gusto", "mi sitio se ve genérico", "por qué todo lo que construyo se ve igual", "hazme un sistema de diseño", "elige mis colores y fuentes", "lo mío parece hecho por una IA", "ayúdame a elegir una fuente", "define los colores de mi marca" o escriba /design-taste.
---

# Design Taste — roba como un diseñador, déjalo por escrito

Nadie nace con buen gusto. El buen gusto es un conjunto de decisiones que alguien ya tomó, escritas para que dejes de volver a decidir cada vez. Este skill mira 1-3 sitios que ya te gustan, extrae las decisiones reales que hay dentro (códigos hex, combinación de fuentes, pasos de espaciado, cuánto espacio vacío, qué tan grande es el titular comparado con el cuerpo) y las escribe en un archivo. A partir de ahí, cada proyecto lee ese archivo, y tus páginas empiezan a verse como si vinieran de la misma persona — porque así es.

## Configuración
Ninguna — este skill CREA el archivo de diseño que leen otros skills.

## Pasos

### 1. Consigue 1-3 referencias y una oración sobre la sensación
Pregunta exactamente esto, en un solo mensaje:

> "Nombra o pega 1-3 sitios cuyo aspecto te encante. Cualquier sitio — una marca a la que le compras, una landing page que guardaste en favoritos, un portafolio. Si tienes capturas, súbelas. Luego completa esta oración: 'Quiero que la gente sienta ___ cuando llegue a mi página.'"

Reglas:
- Si te dan una URL, descarga la página y lee los valores reales del CSS donde puedas. Si no puedes descargarla, dilo claramente y trabaja con lo que sabes del sitio más su captura.
- Si te dan una captura, lee los colores y la tipografía a partir de la imagen.
- Si dicen "no conozco ninguno", no te detengas. Ofrece seis direcciones con nombre y deja que elijan una: **impreso editorial** (titulares grandes con serif, papel crema, un color de tinta), **utilitario suizo** (retícula ajustada, una sans en negrita, mucho blanco), **minimalismo cálido** (blanco roto, sombras suaves, un acento apagado), **técnico oscuro** (casi negro, tipografía monoespaciada, un color de señal brillante), **póster retro** (tipografía display gruesa, dos colores planos, bordes duros), **lujo discreto** (márgenes enormes, tipografía pequeña, casi sin color).
- Nunca aceptes más de 3 referencias. Cuatro referencias son un mood board, no un sistema.

### 2. Aplica ingeniería inversa a las decisiones, no a la vibra
Para cada referencia, anota lo concreto. Di lo que realmente ves:
- **Colores:** el fondo de la página, el color principal del texto, el único acento y cualquier color de superficie/tarjeta. Da códigos hex. La mayoría de los buenos sitios usan 4-6 colores en total, y el acento aparece en menos del 10% de la página.
- **Tipografía:** la fuente display (titulares) y la fuente del cuerpo. Nombra ambas. Anota si es serif + sans, sans + sans o sans + mono.
- **Salto de tamaño:** la proporción entre el titular grande y el texto del cuerpo. Los buenos sitios son seguros — un titular suele ser 3-5 veces el tamaño del cuerpo, no 1.5 veces.
- **Espaciado:** cuánto aire hay arriba y abajo de las secciones. Anota si es ajustado o generoso.
- **Esquinas y bordes:** esquinas rectas, radio pequeño o forma de píldora. Elige uno, nunca se mezclan.
- **Lo que NO hace.** Esto importa más que todo lo demás. Anota las ausencias: sin degradados, sin sombras paralelas, sin íconos, sin fotos de stock de gente en oficinas.

Luego di una línea honesta sobre qué tienen en común las referencias. Si no tienen nada en común, díselo al usuario y haz que elija cuál gana.

### 3. Construye el sistema
Convierte las observaciones en un conjunto de decisiones con nombre. Usa exactamente estos espacios:

- **Paleta:** `ink` (texto principal), `paper` (fondo de la página), `surface` (tarjetas/paneles), `accent` (el único color que significa "actúa"), `muted` (texto secundario). Cinco códigos hex, no más. Comprueba que `ink` sobre `paper` sea de verdad oscuro sobre claro o claro sobre oscuro — si el contraste se ve débil, corrígelo y di por qué.
- **Tipografía:** una fuente display y una fuente de cuerpo, ambas de Google Fonts para que carguen gratis sin configuración. Da la línea exacta de inserción de Google Fonts. Incluye una pila de respaldo.
- **Escala:** seis tamaños, en rem, construidos sobre una proporción. Ejemplo con una proporción de 1.333: 0.875 / 1 / 1.333 / 1.777 / 2.369 / 3.157. Indica la proporción que elegiste.
- **Espaciado:** una unidad base (normalmente 8px) y los pasos que salen de ella: 8 / 16 / 24 / 40 / 64 / 96. Cada espacio de cada página usa uno de estos números y ningún otro.
- **Radio, bordes, sombra:** un valor para cada uno, o la palabra "ninguno".
- **Movimiento:** una duración (150-250ms) y una curva de aceleración. Solo transforms y opacity.

Escribe también la **lista de No hacer**, y pon esto en ella con nombre propio todas y cada una de las veces:

> Nunca el degradado genérico de IA de morado a azul. Es la firma visual de una página en la que nadie pensó. Si un proyecto alguna vez recurre a `#6366f1` fundiéndose en `#a855f7`, detente y usa en su lugar el acento de este archivo.

Agrega tres o cuatro "no hacer" más, sacados de lo que las referencias evitaban.

### 4. Genera una vista previa de muestras que realmente puedan ver
Un sistema de diseño que nadie mira se ignora. Escribe una vista previa en un solo `index.html` autocontenido para que puedan abrirlo en un navegador y ver la cosa. Constrúyelo con estas restricciones:

- Un solo archivo. Sin herramientas de build. Sin librerías JS externas.
- Google Fonts es el único recurso externo, cargado con un `<link>` normal.
- Muestra: las cinco muestras de color con sus códigos hex impresos encima, los seis tamaños tipográficos con la fuente real, una regla de espaciado que muestra los seis pasos como barras apiladas, un botón de ejemplo, una tarjeta de ejemplo y un bloque de ejemplo de titular más párrafo para que vean la combinación en uso real.
- Texto de ejemplo real. Escribe oraciones de verdad sobre lo suyo. Nunca lorem ipsum.
- Cualquier ícono es SVG en línea.
- Totalmente legible con JavaScript desactivado. Mobile first — tiene que verse bien en un teléfono.
- Cualquier animación usa solo transforms y opacity. Sin desenfoque animado, sin filtros de ruido, sin marquesinas.

### 5. Muéstralo y luego toma una ronda de reacciones
Dile al usuario que abra el archivo de vista previa y te dé una reacción en lenguaje simple. No código — una sensación. "Demasiado frío." "La fuente del titular se esfuerza demasiado." "Me encanta el color, odio el espaciado." Haz una ronda de cambios a partir de eso, guarda ambos archivos otra vez y detente. Una ronda es suficiente. Pueden cambiarlo después; lo importante es tener un archivo.

## Resultado — guárdalo

Escribe dos archivos:

1. `~/.claude/design.md` — el sistema en markdown simple. Estructúralo exactamente así para que otros skills puedan leerlo de forma confiable:

```markdown
# Mi sistema de diseño

## Sensación
<su oración>

## Referencias
- <sitio> — lo que tomé de él

## Paleta
- ink: #1C1B17
- paper: #F7F4ED
- surface: #FFFFFF
- accent: #C8492B
- muted: #6B6862

## Tipografía
- Display: Fraunces (Google Fonts) — respaldo: Georgia, serif
- Cuerpo: Inter (Google Fonts) — respaldo: system-ui, sans-serif
- Inserción: <link href="https://fonts.googleapis.com/css2?family=Fraunces:wght@600&family=Inter:wght@400;600&display=swap" rel="stylesheet">

## Escala (proporción 1.333)
0.875rem / 1rem / 1.333rem / 1.777rem / 2.369rem / 3.157rem

## Espaciado (base 8px)
8 / 16 / 24 / 40 / 64 / 96

## Detalles
- Radio: 4px
- Borde: 1px sólido, ink al 12% de opacidad
- Sombra: ninguna
- Movimiento: 180ms ease-out, solo transform y opacity

## No hacer
- Nunca el degradado de IA de morado a azul
- <3-4 más>

## Cómo usar esto
Pega en cualquier prompt de construcción: "Lee ~/.claude/design.md y usa esa paleta, combinación de fuentes, escala y espaciado. Sigue la lista de No hacer."
```

2. `~/.claude/design-preview/index.html` — la página de muestras.

Diles ambas rutas. Luego dales la única siguiente acción, con estas palabras exactas:

> "Abre `~/.claude/design-preview/index.html` en tu navegador. De ahora en adelante, empieza cualquier prompt de construcción con: 'Lee ~/.claude/design.md y síguelo.'"

## Ejemplo (entrada → salida)

**Entrada:** "Me gusta cómo se ve el sitio de Stripe y el de este tostador de café. Quiero que la gente sienta que sé lo que hago. No tengo idea de qué fuentes me gustan."

**Salida (guardada en `~/.claude/design.md`):**
- **Sensación:** competencia tranquila — limpio, no corporativo.
- **Lo que comparten los dos:** fondo casi blanco, texto casi negro, exactamente un acento, un salto enorme entre titular y cuerpo, ninguna sombra paralela en ningún lado.
- **Paleta:** ink `#161616`, paper `#FAFAF8`, surface `#FFFFFF`, accent `#B4472A`, muted `#71706B`.
- **Tipografía:** Display = Fraunces 600. Cuerpo = Inter 400/600. Titular serif sobre cuerpo sans — esa combinación hace la mayor parte del trabajo.
- **Escala:** proporción 1.333. Titular `3.157rem`, cuerpo `1rem`. Es un salto de 3.1 veces, y por eso se lee con seguridad.
- **Espaciado:** base 8. Las secciones llevan 96 arriba y abajo. Nada en la página usa un número fuera de la escalera.
- **No hacer:** nunca el degradado de IA de morado a azul; sin sombras paralelas; sin fotos de stock de gente frente a laptops; nunca más de un color de acento en una pantalla.

Y `~/.claude/design-preview/index.html` se abre con cinco bloques de color etiquetados, los seis tamaños tipográficos en Fraunces e Inter, una pila de barras de espaciado y una tarjeta de ejemplo con un titular y un botón reales.

## Notas / casos especiales
- El error de principiante que esto evita: volver a decidir colores y fuentes desde cero en cada proyecto, de modo que nada de lo que hacen parece relacionado. Decidir una vez es todo el punto.
- Si dan referencias que se pelean entre sí (un sitio de póster brutalista y una marca suave de bienestar), nombra el conflicto en voz alta y haz que elijan cuál manda. No las promedies — el diseño promediado es lo que significa "genérico".
- Si odian todo lo que propones, eso es información, no un fracaso. Pregunta "¿qué se siente mal específicamente — el color, la fuente o la cantidad de espacio?" Una palabra suya basta para redirigir.
- Si ya tienen un logo o un color de marca que deben conservar, ese color se convierte en `accent` y todo lo demás se construye alrededor de él.
- Una vez que este archivo exista, pasa a **make-it-designed** para aplicarlo a algo que ya construyeron, o a **mobile-check** para asegurarte de que sobreviva en un teléfono.
