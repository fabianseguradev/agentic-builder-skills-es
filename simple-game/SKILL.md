---
name: simple-game
description: Construye un juego de navegador jugable en una sola sentada — un archivo, se abre en cualquier navegador, funciona en un teléfono, sin cuentas ni bases de datos. Elige de un menú de clásicos etiquetados según cuánto toman, luego hazlo tuyo con un cambio de temática, un giro, tu nombre en la pantalla de título y un puntaje máximo guardado. Úsalo cuando el usuario diga "/simple-game", "constrúyeme un juego", "quiero hacer un juego", "haz un juego de navegador", "podemos construir snake", "construye un juego que pueda mandarle a mis amigos", "algo divertido para construir", "no sé qué construir primero", "haz un juego con Claude" o "construye un juego que pueda jugar mi hijo".
---

# Simple Game — la mejor primera cosa que vas a construir

Un juego es la mejor primera construcción, y no porque sea fácil. Es la mejor porque no te puedes mentir a ti mismo sobre si funciona. A los sitios web les dan un encogimiento de hombros. Los juegos se juegan. Y un juego es un solo archivo sin login, sin base de datos y nada que configurar — así que lo único entre tú y algo real es describirlo bien.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Di por qué un juego primero
Ábrelo con esto, corto, con tus propias palabras:

- **O funciona o no.** No hay que preguntarse si es bueno. Presionas una tecla, la cosa se mueve o no se mueve. Ese ciclo de retroalimentación enseña más en una noche que una semana de lectura.
- **La gente de verdad juega juegos.** Mándale a alguien tu sitio web y dice "lindo." Mándale un juego y lo juega, y luego te manda su puntaje. Esa reacción es lo que mantiene a un principiante construyendo.
- **Es un solo archivo autocontenido.** Sin base de datos, sin cuentas, sin pagos, sin servidor. Todo vive en un único `index.html` que le puedes mandar a alguien por email.

Luego: "Elige uno de esta lista, o cuéntame un juego que te encantaba y construimos ese."

### 2. Ofrece el menú
Muestra unos ocho, con etiquetas de tiempo honestas. Diles que el tiempo es para la versión que funciona, no la versión pulida.

**15 minutos**
- **Clicker** — haces clic en la cosa, el número sube, compras mejoras. El ciclo más simple posible, y raramente adictivo.
- **Encuentra el par** — das vuelta cartas, encuentras pares. Ideal para cambiarle la temática con tus propias imágenes.
- **Whack-a-mole** — cosas aparecen, las tocas, el tiempo corre. Funciona muy bien en un teléfono.

**1 hora**
- **Snake** — creces, no te choques contigo mismo. El clásico primer juego, con razón.
- **Breakout** — rebotas una bola, rompes ladrillos. Te enseña qué significa "colisión" sin que aprendas la palabra.
- **Tocador estilo Flappy** — una sola entrada, sin fin, brutalmente difícil. Muy compartible.

**Una noche**
- **Plataformas (un nivel)** — corres, saltas, llegas a la bandera. Lograr que el salto se sienta bien toma iteración; esa es la lección.
- **Torre de defensa (un mapa, tres oleadas)** — colocas cosas, las ves pelear. La construcción más grande de aquí; hazla segunda, no primera.

Si nombran un juego que no está en la lista, tómalo, y di con honestidad en qué grupo cae. Si eligen "una noche" y es su primerísima construcción, di claramente que uno de 1 hora terminado esta noche le gana a uno de una noche abandonado al 60%.

### 3. Escribe la especificación de juego de 4 secciones
No empieces a construir a partir de un pedido de una línea. Complétalo con ellos primero — toma dos minutos y ahorra una hora. Cuatro secciones, y la redacción de cada una importa.

**1. CONTENEDOR**
> Un solo `index.html` autocontenido. Sin herramientas de build, sin librerías de JavaScript externas. Solo Google Fonts — una fuente display, una fuente para el cuerpo. Un color de acento más neutros, nunca el degradado de morado a azul. Área de juego fija, centrada, que cabe en la pantalla de un teléfono sin desplazarse. Funciona con toque y con teclado.

**2. JUGABILIDAD — una regla por viñeta**
Aquí es donde los principiantes se vuelven vagos y hacen un desastre. Cada viñeta es una sola regla, dicha llanamente. Nada de párrafos. Ejemplo para Snake:
> - La serpiente se mueve un cuadro cada 120ms en la dirección que mira.
> - Las flechas y los deslizamientos cambian la dirección. No puede revertirse contra sí misma.
> - Comer una manzana hace crecer la serpiente un cuadro y suma 1 punto.
> - Chocar contra una pared o contra su propio cuerpo termina el juego.
> - Aparece una manzana nueva en un cuadro vacío al azar.

De diez a quince viñetas así son un juego completo. Escríbelas juntos, reléanlas y pregunta: "¿Alguna viñeta está haciendo dos cosas?" Divídela si es así.

**3. UI — solo ubicación, sin hablar de estilos**
> Puntaje arriba a la izquierda. Puntaje máximo arriba a la derecha. Una pantalla de inicio con el título y "Presiona espacio o toca para jugar." Un panel de fin de juego con el puntaje, el mejor puntaje y un botón de reinicio. Nada más en pantalla.

**4. EL REMATE**
Termina siempre la especificación con esta línea, exactamente:
> Muéstrame una vista previa en vivo cuando se ejecute.

Esa sola oración es la diferencia entre adivinar y ver.

Para sonido, si lo quieren: **"Web Audio API, sin archivos externos."** Pitidos simples generados en el navegador — nada que descargar, nada que se rompa. Para cualquier cosa guardada entre sesiones: **"guardar en localStorage."**

### 4. Constrúyelo, luego júgalo
Construye el juego a partir de la especificación. Guarda en `~/games/<slug>/index.html`. Crea la carpeta.

Ábrelo:

```bash
open ~/games/<slug>/index.html
```

Luego: "Juégalo. No seas amable con él. ¿Qué se sintió mal?"

Haz el ciclo en lenguaje simple, de 5 a 10 rondas. La sensación del juego es casi enteramente iteración. Las notas reales suenan así:
- "Es demasiado rápido para reaccionar."
- "El salto se siente flotante."
- "Sigo muriendo al instante y no sé por qué."
- "Nada me dice que anoté."

Describe el síntoma, nunca toques el código. Cada un par de rondas, ofrece guardarlo como un punto de control para que una mala idea no les cueste la versión que funciona.

### 5. La pasada de "hazlo tuyo"
Un clon que funciona es un tutorial. Un clon que funciona con tu huella es algo que hiciste. Haz las cinco:

- **Cámbiale la temática.** Cambia el tema a algo de su vida real. Snake se convierte en un salchicha persiguiendo premios. Breakout se convierte en emails que estás borrando. Whack-a-mole se convierte en tu bandeja de entrada a las 9am. Este solo cambio hace que la gente lo reenvíe.
- **Un giro mecánico.** Exactamente uno. Un power-up, un momento de controles invertidos, un cuadro que te acelera, un modo que invierte la gravedad cada 10 segundos. Un giro lo hace suyo. Dos lo hace confuso.
- **Su nombre en la pantalla de título.** "SNAKE — por Maya." Pequeño, pero este es el punto de todo el ejercicio.
- **Puntaje máximo guardado en localStorage.** Para que el número siga ahí mañana. Esto es lo que convierte una demo en un juego.
- **Un botón de compartir.** Copia una línea al portapapeles: "Anoté 47 en Treat Chase. Supérame: <url>." Completa la URL después de desplegarlo.

### 6. Guarda las notas y pasa el relevo
Escribe `~/games/<slug>/NOTES.md` con las viñetas de la especificación, el giro y una línea para la próxima vez.

Cierra con: "Ejecuta **deploy-it** para tener un link real, y luego mándaselo a tres personas esta noche y pídeles su puntaje. Feo pero en línea le gana a bonito pero guardado en una carpeta."

## Resultado — guárdalo
- `~/games/<slug>/index.html` — el juego jugable, un archivo, teléfono y teclado.
- `~/games/<slug>/NOTES.md` — las reglas de jugabilidad, el giro y el siguiente paso.

Indica ambas rutas. Única siguiente acción: ejecutar **deploy-it**, luego mandárselo a tres personas y pedirles su puntaje.

## Ejemplo (entrada → salida)
**Entrada:** "Quiero construir un juego pero no tengo idea de cuál. Quizás algo con mi perro."

**Salida (Snake, con temática cambiada, guardado en `~/games/treat-chase/index.html`):**

Pantalla de título: **TREAT CHASE — por Maya.** Presiona espacio o toca para jugar.

La especificación que lo construyó, en `NOTES.md`:
- El salchicha se mueve un cuadro cada 120ms en la dirección que mira.
- Las flechas y los deslizamientos cambian la dirección. No puede revertirse contra sí misma.
- Comer un premio la hace crecer un cuadro y suma 1 punto.
- Cada quinto premio es dorado, vale 3 puntos y desaparece después de 4 segundos. *(el giro)*
- Chocar contra una pared o contra su propio cuerpo termina el juego.
- Puntaje máximo guardado en localStorage.
- Sonido: un pitido corto al comer, uno más grave al morir. Web Audio API, sin archivos externos.

Panel de fin de juego: puntaje, mejor de siempre, botón de reinicio y un botón de **Copiar mi puntaje**.

## Notas / casos especiales
- El error que esto evita: que la primera construcción de un principiante sea algo sin un estado de victoria claro, así que no pueden saber si funcionó y pierden el impulso. Un juego te lo dice de inmediato.
- Si su idea necesita multijugador, cuentas o perfiles guardados entre dispositivos, di claramente que eso es una construcción con servidor y no es para esta noche. Ofrece la versión de un jugador ahora y anota el resto en `NOTES.md`.
- Si una viñeta de regla está haciendo dos cosas, divídela antes de construir. Las viñetas vagas son donde los juegos van mal, no el código.
- Si se traban con la sensación del juego, cambia un número a la vez — velocidad, o gravedad, o tamaño. Cambiar tres a la vez significa que no aprenden nada.
- Derivación: **deploy-it** para publicar y conseguir la URL para compartir. **first-website** si quieren una página alrededor del juego. **link-in-bio** si quieren el juego como uno de sus links públicos.
