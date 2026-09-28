---
name: mobile-check
description: Revisa una página que construiste tal como la vería realmente una persona en un teléfono, y recibe una lista numerada de arreglos ordenada según cuánto te cuesta cada problema. Detecta texto diminuto, botones demasiado pequeños para tocar, cosas que se deslizan hacia los lados fuera de la pantalla, imágenes que desarman el diseño y un botón principal al que nadie llega con el pulgar. Cada arreglo viene con la oración exacta para pegarle de vuelta a Claude. Úsalo cuando el usuario diga "revisa esto en móvil", "mi sitio funciona en un teléfono", "se ve roto en mi teléfono", "por qué mi página se mueve de lado", "la versión móvil está mal", "prueba mi página en móvil", "mi texto se ve diminuto en el teléfono" o escriba /mobile-check.
---

# Mobile Check — mira tu página como la va a ver la mayoría

La construiste en una laptop. La mayoría de las personas que la visiten estarán en un teléfono, con una mano, con una conexión lenta, medio distraídas. Una página que se ve bien a 1440px de ancho puede ser inutilizable a 375px, y nunca lo sabrías porque nunca la miraste. Esto lee tu página, encuentra lo que se rompe en un teléfono y te devuelve una lista numerada ordenada según cuánto daño hace cada cosa — con la oración exacta para pegarle de vuelta a Claude y que lo arregle.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Consigue la página y fija el marco
Pide la ruta del archivo. Si no la saben, encuentra el `index.html` en el que han estado trabajando y confírmalo antes de leerlo.

Lee todo el archivo — el HTML, el CSS que contiene y cualquier JavaScript en línea. Luego fija el marco en voz alta:

> "Voy a leer esto como un teléfono de 375 píxeles de ancho — es un iPhone promedio. Todo lo que sigue es lo que se rompe a ese tamaño."

Si tienen una URL en vivo y hay una herramienta de navegador disponible, ábrela a 375x812 y mírala. Si no, lee el código con atención — casi todos los fallos en móvil se ven en el CSS.

### 2. Haz las siete revisiones
Recórrelas en orden. Para cada una, enumera cada infractor específico con el elemento y el valor que encontraste.

**1. Scroll lateral (el peor).** Si la página se desliza a la izquierda y a la derecha, todo lo demás es una nota al pie. Busca: anchos fijos en píxeles mayores a 375 (`width: 600px`), `min-width` en contenedores, tablas, cadenas largas sin cortes como URLs o emails, `100vw` combinado con padding, márgenes negativos, elementos con posición absoluta empujados más allá del borde derecho e imágenes sin `max-width: 100%`. Revisa también si falta `<meta name="viewport" content="width=device-width, initial-scale=1">` — sin esa línea toda la página se muestra alejada y diminuta, y es la causa más común de todas.

**2. Zonas táctiles.** Todo lo que se toca — botones, links en fila, elementos de navegación, controles de formulario, botones de ícono — necesita al menos 44x44 píxeles de área táctil real, con al menos 8px de espacio entre eso y lo siguiente que se puede tocar. Señala: botones pequeños de solo ícono, links de texto apretados en una lista, botones de cerrar diminutos y casillas de verificación de tamaño por defecto. El pulgar de una persona mide unos 10mm de ancho y no está apuntando con cuidado.

**3. Texto demasiado pequeño.** Texto del cuerpo de menos de 16px. No es una opinión de estilo — por debajo de 16px, los teléfonos pueden hacer zoom en la página cuando alguien toca un campo de formulario, lo que desplaza el diseño hacia un lado. Señala cada font-size de menos de 16px en el texto del cuerpo, y cualquier cosa de menos de 14px en cualquier lugar. Señala también las líneas que van de borde a borde sin respiro, y un interlineado de menos de 1.4 en el texto del cuerpo.

**4. Imágenes que empujan el diseño.** Cada imagen necesita `max-width: 100%; height: auto;`. Señala imágenes de ancho fijo, imágenes de fondo con tamaños fijos, imágenes sin atributos `width`/`height` (lo que hace que la página salte mientras carga) y cualquier archivo de imagen claramente enorme para un teléfono. Comprueba también que cualquier cosa con texto incrustado siga siendo legible en pequeño — normalmente no lo es.

**5. Alcance del pulgar en la acción principal.** ¿Dónde está el único botón que quieres que toquen? Con un teléfono sostenido con una mano, la zona fácil son los dos tercios inferiores de la pantalla, y el lugar más difícil de alcanzar son las esquinas superiores. Señala: un botón principal que solo está en el encabezado, un botón principal que solo aparece después de un scroll largo sin repetirse y cualquier acción crítica ubicada en una esquina superior. El arreglo suele ser repetir el botón principal más abajo, o fijarlo en la parte inferior.

**6. ¿Se lee con JavaScript desactivado?** Desactiva JS en tu cabeza y vuelve a leer la página. Señala cualquier cosa que solo aparezca mediante script: contenido revelado por un acordeón o una pestaña, imágenes que cargan de forma diferida con JavaScript sin alternativa, animaciones que empiezan los elementos en `opacity: 0` y nunca los restauran si el script falla, y menús que no se abren. El titular, la oferta y el link principal tienen que estar ahí sin que se ejecute ningún script.

**7. Todo lo demás que le cuesta visitantes reales.** Retículas de varias columnas que nunca se colapsan a una. Padding horizontal de menos de 16px, de modo que el texto toca el borde de la pantalla. Encabezados fijos que ocupan más de un 15% de la altura de la pantalla. Interacciones que solo funcionan con hover — los teléfonos no tienen hover, así que todo lo que solo aparece al pasar el mouse es invisible. Formularios con el teclado equivocado (un campo de email debería usar `type="email"`, uno de teléfono `type="tel"`). Elementos con posición fija tapando contenido. Tamaños de fuente definidos en unidades `vw` que se vuelven ilegibles en anchos pequeños.

### 3. Ordena por daño, no por esfuerzo
Clasifica cada problema que encontraste en este orden y numéralos 1, 2, 3...:

1. **Mata la página** — scroll lateral, falta la etiqueta viewport, contenido invisible sin JS, el botón principal inalcanzable o ausente.
2. **Te cuesta el visitante** — zonas táctiles demasiado pequeñas, texto del cuerpo de menos de 16px, imágenes que desarman el diseño, formularios que son una tortura de completar.
3. **Se ve sin terminar** — padding apretado, columnas que no se colapsaron, interlineado débil, detalles agradables que solo funcionan con hover.

No rellenes la lista. Si encontraste cuatro problemas reales, da cuatro. Una lista falsa les enseña a ignorar los reales.

### 4. Escribe la oración para pegar de vuelta de cada arreglo
Esta es la parte que hace útil al skill. Para cada problema numerado, escribe una oración en lenguaje simple que el usuario pueda copiar y pegarle directamente a Claude. Describe el síntoma y el resultado — nunca el código. Ese es el movimiento de principiante: describir lo que viste, no intentar editar CSS.

Buenas oraciones para pegar de vuelta:
- "En mi teléfono la página se desliza a la izquierda y a la derecha. Haz que nada se desplace hacia los lados a 375px de ancho."
- "El botón 'Reservar ahora' es demasiado pequeño para tocarlo en un teléfono. Haz que cada botón y cada link tenga al menos 44px de alto, con espacio entre ellos."
- "El texto del cuerpo es demasiado pequeño para leerlo en un teléfono. Pon el texto del cuerpo en al menos 16px con un interlineado de 1.6."
- "Mi imagen principal se sale por el costado de la pantalla en un teléfono. Haz que todas las imágenes se encojan para caber en su contenedor."
- "El único botón 'Empezar' está arriba de todo. Agrega el mismo botón otra vez cerca del final de la página para no tener que volver a subir."
- "Agrega la etiqueta viewport para móviles en el head de la página para que no se vea alejada en los teléfonos."

Malas — nunca escribas estas: cualquier cosa con un selector, un nombre de propiedad o un valor en píxeles que tendrían que entender.

### 5. Diles cuál hacer primero
Termina con el único arreglo de mayor valor y nada más. Una tarea por prompt. Diles que peguen esa única oración, vuelvan a mirar la página y luego regresen por la siguiente. Arreglar las ocho en un solo prompt es como una página que funciona se convierte en una rota.

Recuérdales: `/rewind` deshace cualquier cambio, así que probar un arreglo no cuesta nada.

## Resultado — guárdalo

Escribe el informe completo en `~/mobile-checks/<page-name>-<date>.md` con:
- La ruta de la página y el ancho que revisaste.
- La lista numerada de problemas, cada uno con: qué está mal, dónde está en la página, por qué les cuesta y la oración para pegar de vuelta en un bloque copiable.
- Una lista corta de "ya está bien" — las cosas que pasaron la revisión. La gente necesita saber qué no tocar.
- El único arreglo para hacer primero.

Diles la ruta, y luego:

> "Copia el arreglo #1 y pégalo como tu próximo mensaje. Luego vuelve a mirar la página y regresa por el #2."

## Ejemplo (entrada → salida)

**Entrada:** "Hice una página para mi negocio de limpieza y mi hermana dice que se ve rara en su teléfono. Está en ~/cleaning/index.html."

**Salida (guardada en `~/mobile-checks/cleaning-2026-07-30.md`):**

**1. La página se ve alejada y diminuta.** No hay etiqueta viewport en el head, así que los teléfonos la muestran con ancho de escritorio y lo encogen todo. Por eso tu hermana dijo que se ve rara — es una sola línea que falta.
> "Agrega la etiqueta viewport para móviles en el head de la página para que no se vea alejada en los teléfonos."

**2. La página se desplaza hacia los lados.** La tabla de precios está definida con `width: 720px`, que es más ancha que la pantalla de un teléfono, así que toda la página se arrastra a la izquierda y a la derecha.
> "Mi tabla de precios hace que la página se desplace hacia los lados en un teléfono. Haz que en pantallas pequeñas se apile como una lista simple en lugar de una tabla ancha."

**3. El botón "Pedir cotización" es demasiado pequeño para tocarlo.** Mide 28px de alto y está a 4px del link del número de teléfono, así que la gente va a tocar el equivocado.
> "El botón 'Pedir cotización' es demasiado pequeño para tocarlo en un teléfono. Haz que cada botón y cada link tenga al menos 44px de alto, con 12px de espacio entre ellos."

**4. El texto del cuerpo es de 14px.** Es difícil de leer, y hace que los iPhone hagan zoom cuando alguien toca el formulario.
> "El texto del cuerpo es demasiado pequeño para leerlo en un teléfono. Pon el texto del cuerpo en al menos 16px con un interlineado de 1.6."

**Ya está bien:** las imágenes tienen `max-width: 100%`, la página se lee bien con JavaScript desactivado, las columnas se colapsan a una en pantallas pequeñas y el número de teléfono usa `type="tel"`.

**Hazlo primero:** el #1. Es una línea y puede que arregle la mitad de lo que ella vio.

## Notas / casos especiales
- El error de principiante que esto evita: construir en una laptop, probar en una laptop y lanzar algo que la mayoría de los visitantes literalmente no puede usar.
- Si la página no tiene la meta etiqueta viewport, siempre es el #1 y deberías decir claramente que varios de los otros problemas de la lista pueden desaparecer una vez que se agregue.
- Si no pueden darte una ruta de archivo pero tienen una URL en vivo, trabaja a partir de la URL. Si no tienen ninguna de las dos, pide una captura de pantalla desde su teléfono real y léela.
- Si la página es un solo párrafo de texto sin estilos, di que está bien y no inventes problemas. Un informe corto y honesto genera confianza en los largos.
- Si la página es fea en lugar de estar rota, ese es otro trabajo — pasa a **make-it-designed**.
