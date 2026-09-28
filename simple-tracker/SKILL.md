---
name: simple-tracker
description: Construye un pequeño tracker o panel personal que funciona por completo en tu navegador y guarda tus datos en tu propia máquina — hábitos, entrenamientos, pipeline de clientes, lista de lectura, dinero que entra, cualquier cosa que ahora mismo lleves en una hoja de cálculo desordenada. Sin login, sin base de datos, sin factura mensual, un solo archivo HTML que abres como un marcador. Úsalo cuando el usuario diga "constrúyeme un tracker", "tracker de hábitos", "quiero un panel para mis cosas", "reemplaza mi hoja de cálculo", "algo para registrar mis entrenamientos", "seguimiento de mis clientes", "panel personal", "app para llevar un registro de", "app de lista de lectura" o escriba /simple-tracker.
---

# Simple Tracker — un archivo, tus datos, sin factura

Lo que la mayoría de la gente quiere de una app es una lista a la que pueda agregar cosas y un número que le diga cómo va. Eso no necesita un login, una base de datos ni $12 al mes — necesita un solo archivo HTML que se guarda en tu propio navegador. Esto construye eso. También es el mejor segundo proyecto que puede hacer un principiante, porque lo usas todos los días, así que de verdad notas qué mejorar.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Elige qué rastrear
Pregunta qué llevan en la cabeza o en una hoja de cálculo desordenada ahora mismo. Si no tienen respuesta, dales este menú y deja que elijan uno. Cada uno viene con un texto de partida que pueden usar como descripción:

- **Tracker de hábitos** — "Una fila por hábito, una casilla para cada día de la semana actual, y un número grande arriba que muestra mi racha actual más larga."
- **Registro de entrenamientos** — "Agrego un ejercicio con series, repeticiones y peso. Muestra mis últimas cinco sesiones y, arriba, el peso total que moví esta semana comparado con la semana pasada."
- **Pipeline de clientes** — "Cada cliente es una tarjeta con un nombre, cuánto paga y una etapa: lead, en conversación, propuesta enviada, cerrado, muerto. El número grande arriba es el dinero total en las columnas 'propuesta enviada' y 'cerrado'."
- **Lista de lectura** — "Agrego un libro con título y autor. Cada uno está en quiero-leer, leyendo, o terminado. El número de arriba es cuántos he terminado este año."
- **Dinero que entra** — "Registro un pago con quién, cuánto y la fecha. El número de arriba es el total de este mes junto al total del mes pasado."
- **Registro de contenido** — "Registro un post con la plataforma, la fecha y el gancho. El número de arriba es cuántos he publicado en los últimos 30 días."

Sea cual sea el que elijan, haz una pregunta de seguimiento: "¿Cuál es el único número que querrías ver en el segundo que lo abres?" Esa respuesta se convierte en la parte de arriba de la página y da forma a todo lo demás.

### 2. Fija la forma — un agregar, una lista, un número
Todo buen tracker pequeño tiene las mismas tres partes. Dilas en voz alta para que el usuario aprenda la forma, no solo reciba un archivo:

1. **Una cosa que agregas.** Una sola fila de campos arriba, o un botón que abre un pequeño formulario. Dos o tres campos como máximo. Si agregar una entrada toma más de unos ocho segundos, van a dejar de usarlo en menos de una semana, y un tracker que no se usa es peor que la hoja de cálculo.
2. **Una lista que ves.** Lo más reciente primero. Cada fila muestra solo lo que querrían escanear, más una forma de editar y una de borrar. Nada más.
3. **Un número arriba que te dice cómo vas.** Grande, imposible de no ver y honesto. No tres gráficos. Un número, con una línea pequeña de contexto debajo — "12 este mes · 9 el mes pasado."

Resístete al desbordamiento de alcance aquí, una vez y con claridad. Los principiantes piden etiquetas, filtros, búsqueda, categorías, gráficos y recordatorios en la primera sesión, y luego nunca terminan. Construye las tres partes, úsalo una semana, y luego agrega la única cosa que de verdad les faltó. Ese es el ciclo.

### 3. Define bien el modelo de datos, y luego dilo en lenguaje simple
Antes de construir, diles exactamente qué contiene una entrada, en palabras:

> "Una entrada es: un nombre, un número, una fecha y un estado. Eso es todo. Todo en la página se construye a partir de esas cuatro cosas."

Luego decide lo pequeño de antemano:
- Qué cuenta como duplicado, si algo cuenta.
- En qué orden se ordena la lista.
- Qué está calculando realmente el número de arriba, dicho como una oración: "cuántas entradas tienen estado 'terminado' y una fecha de este año."
- Qué muestra la página cuando todavía no hay nada — el estado vacío. Esto importa más de lo que la gente cree, porque es lo primero que van a ver. Escribe una línea amigable más una pista de qué escribir.

### 4. Constrúyelo
Un archivo. Incluye cada una de estas cosas:

- Un solo `index.html` autocontenido. Sin herramientas de build, sin librerías JS externas, sin frameworks, sin backend, sin base de datos.
- **Guarda en `localStorage`.** Todos los datos viven en el navegador bajo una clave claramente nombrada. Léela al cargar, escríbela en cada cambio. Guárdala como JSON.
- Google Fonts es el único recurso externo. Una fuente display para el número grande y los encabezados, una fuente para el cuerpo de la lista.
- Paleta contenida: un acento más neutros. **Nunca** el degradado genérico de IA de morado a azul. El acento le pertenece al botón de agregar y al número de arriba, a nada más. Si existe `~/.claude/design.md`, léelo y sigue esa paleta, combinación de fuentes y espaciado.
- Mobile first. Van a usar esto en su teléfono. Campos de al menos 48px de alto, zonas táctiles de al menos 44px, nada se desplaza hacia los lados a 375px de ancho, y el formulario de agregar se alcanza con el pulgar.
- **Legible sin JavaScript.** Con los scripts desactivados, la página sigue mostrando el título, para qué es el tracker y la explicación del estado vacío, en lugar de una pantalla en blanco.
- Anima solo con transforms y opacity. Una fila nueva puede aparecer y deslizarse en unos 150ms. Sin desenfoque animado, sin filtros de ruido, sin marquesinas, nada en bucle.
- Texto real — las etiquetas reales para su tracker real. Nunca lorem ipsum.
- Íconos SVG en línea. Borrar recibe una pequeña confirmación para que un toque equivocado no borre una fila.
- Meta etiqueta viewport y un `<title>` real, para que se vea bien guardado en la pantalla de inicio de un teléfono.
- **Botones de exportar e importar.** Exportar descarga sus datos como un archivo JSON. Importar lee uno de vuelta. Este es el intercambio honesto de `localStorage`: los datos viven en un navegador en un dispositivo, y borrar los datos de navegación puede eliminarlos. Dos botones pequeños hacen eso sobrellevable. Díselo al usuario claramente en lugar de esconderlo.
- Mantén toda la forma de los datos y el cálculo del número de arriba en un bloque claramente comentado cerca del principio del script, para que quede obvio dónde cambiar cosas más adelante.

### 5. Úsalo antes de mejorarlo
Diles el último paso, y dilo en serio:

- Abrir el archivo, agregar tres entradas reales ahora mismo, y comprobar que el número de arriba está diciendo la verdad.
- Marcarlo como favorito, o en un teléfono agregarlo a la pantalla de inicio para que se abra como una app.
- Usarlo durante una semana sin cambiar nada.
- Luego volver con una oración sobre lo que más les molestó, y cambiar solo eso.

Ese es el ciclo. De cinco a diez rondas pequeñas es normal y es el flujo de trabajo, no una señal de que algo salió mal. Diles también: `/rewind` deshace cualquier cambio, y "guarda esto como un punto de control" hace un guardado permanente al que siempre pueden volver.

## Resultado — guárdalo

Escribe el tracker en `~/tools/<tracker-slug>/index.html`.

Escribe también `~/tools/<tracker-slug>/notes.md` con: qué contiene una entrada, qué calcula el número de arriba en lenguaje simple, el nombre de la clave de `localStorage`, la advertencia de exportar/importar sobre que los datos viven en un solo navegador y una lista corta de "las próximas tres cosas que podría agregar" — para que cuando vuelvan dentro de una semana no empiecen desde una página en blanco.

Diles ambas rutas, y luego:

> "Abre `~/tools/<tracker-slug>/index.html`, agrega tres entradas reales y márcalo como favorito. Úsalo una semana antes de cambiar nada, y luego dime la única cosa que te molestó."

## Ejemplo (entrada → salida)

**Entrada:** "Llevo a mis clientes freelance en una hoja de Google y nunca la abro. Quiero ver qué dinero está entrando de verdad."

**Salida (guardada en `~/tools/client-pipeline/index.html`):**

- **Una entrada contiene:** nombre del cliente, monto mensual, etapa (lead / en conversación / propuesta enviada / cerrado / muerto) y la fecha en que se agregó.
- **Agregar:** una fila arriba — nombre, monto, un desplegable de etapa y un botón "Agregar cliente." Menos de ocho segundos.
- **Lista:** tarjetas lo más reciente primero, agrupadas por etapa, con el monto a la derecha. Toca una tarjeta para cambiar su etapa. Un pequeño borrar con confirmación.
- **El número:** `$4,300 en juego` en tipografía display grande, con una línea más pequeña debajo: "3 propuestas afuera · 2 cerradas · $1,800 ya cerrados."
- **Estado vacío:** "Todavía no hay nada aquí. Agrega el cliente con el que hablaste más recientemente."
- **Aspecto:** fondo hueso, texto casi negro, un acento verde oscuro solo en el botón de agregar y el número grande. Las tarjetas nuevas aparecen y se deslizan en 150ms.
- **Datos:** guardados en `localStorage` bajo `client-pipeline-v1`. Botones de exportar e importar en el pie.
- `notes.md` advierte que los datos viven en este navegador en este dispositivo, les dice que exporten una vez al mes y enumera tres posibles agregados: una fecha de "último contacto", filtrar clientes muertos y un total mensual.

## Notas / casos especiales
- El error de principiante que esto evita: diseñar una app completa con login, base de datos y hosting para algo que va a usar una sola persona, y luego nunca terminarlo.
- `localStorage` es por navegador y por dispositivo. Su teléfono y su laptop van a tener datos distintos, y borrar los datos de navegación los elimina. Dilo claramente y entrega siempre exportar/importar. Nunca insinúes que se sincroniza.
- Si piden cuentas, compartir con un compañero de equipo o acceso desde dos dispositivos, eso es una base de datos real y otro proyecto. Dilo con honestidad en lugar de construirlo a medias. Construye primero la versión de una persona — normalmente resulta ser suficiente.
- Si enumeran ocho funciones en el primer mensaje, construye la forma de tres partes y pon las otras cinco en la lista "próximas tres cosas" de `notes.md`. Pueden tenerlas; solo que no antes de haberlo usado.
- Ejecuta **mobile-check** sobre él después de una semana de uso real, y **make-it-designed** si funciona pero parece una hoja de cálculo con una fuente.
