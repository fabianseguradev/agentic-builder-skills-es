---
name: error-decoder
description: Pega cualquier error, texto en rojo o mensaje que asuste y recibe qué se rompió en lenguaje simple, si puedes ignorarlo y la oración exacta que tienes que pegarle a Claude para arreglarlo. Nunca tocas código. Úsalo cuando el usuario diga "me salió un error", "qué significa esto", "texto en rojo", "dice que algo falló", "creo que lo rompí", "ayuda, estoy atascado", "esto se ve mal", "es grave esto", "puedo ignorar esto", "no se ejecuta", "algo salió mal" o "/error-decoder". Actívalo también cuando alguien pegue un muro de texto técnico sin ninguna pregunta.
---

# Error Decoder — lo traduce y luego te da la oración para arreglarlo

El texto en rojo paraliza a los principiantes. La mayor parte no es un desastre — mucho de eso es una advertencia sobre la que nadie tiene que hacer nada. Este skill lee el error, te dice qué se rompió y qué tan grave es, y te da una oración para pegarle de vuelta a Claude. Nunca abres un archivo ni editas una línea.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Primero tranquiliza, en dos líneas
Antes de cualquier análisis, di dos cosas:
- "Los errores son normales. Todas las personas que construyen algo los ven constantemente. No son una señal de que hiciste algo mal."
- "Nada está roto para siempre. `/rewind` deja tu proyecto como estaba antes del último cambio."

Dilo una vez, claramente. Luego trabaja. No repitas el mensaje tranquilizador en cada párrafo — se lee como condescendiente.

### 2. Consigue el contexto alrededor del error
Pide el texto del error si no lo pegaron, más dos cosas rápidas:
- "¿Qué le acabas de pedir a Claude justo antes de esto?"
- "¿La cosa sigue funcionando, o se detuvo?"

Esa segunda pregunta importa más que el texto del error. Una advertencia en rojo mientras la página sigue cargando bien es una situación completamente distinta de una página que se quedó en blanco.

### 3. Clasifica qué tan grave es
Ponlo exactamente en una de cuatro categorías y di la categoría por su nombre:

- **Ruido.** Una advertencia, un aviso de obsolescencia, una queja de versión, un mensaje de auditoría. No hay nada que hacer. La cosa funciona. Ignóralo y sigue.
- **Cosmético.** Algo se ve mal pero el proyecto funciona. Una imagen que falta, una fuente que no cargó, un estilo roto. Se puede arreglar después, no bloquea esta noche.
- **Bloqueado.** La cosa no se ejecuta o no carga hasta que se arregle. Este es el caso normal y normalmente es una pieza específica que falta.
- **Rebobínalo.** El último cambio empeoró las cosas de una forma enredada. No lo depures — deshazlo e inténtalo por otro camino.

Di la categoría en una oración con la razón: "Esto es Ruido — es una advertencia de versión de una herramienta, y tu página está cargando bien."

### 4. Traduce el error a lenguaje simple
Tres líneas cortas, sin jerga:
- **Qué se rompió:** lo que no funcionó, en palabras de sobremesa. "Intentó abrir un archivo que no está."
- **Por qué:** la razón probable, en una frase. "El archivo se renombró o nunca se creó."
- **Lo que no es:** elimina el miedo que cargan. "Esto no borró nada. Tus otros archivos están intactos."

Si tiene que aparecer un término técnico porque está en el error, defínelo en una frase corta la primera vez. "Un puerto — la puerta numerada que usa tu sitio en tu computadora — ya lo está usando otra cosa."

### 5. Dales la oración exacta para arreglarlo
Este es el entregable. Una oración que copian y le pegan de vuelta a Claude, escrita como habla un director: describe el síntoma, no la reparación.

Buena forma: lo que observaron + dónde + lo que esperaban.
- "Cuando abro la página, está completamente en blanco y la terminal dice 'Cannot find module express'. Funcionaba antes de que agregaras el formulario de contacto. Arréglalo."
- "El sitio carga pero la imagen del encabezado no aparece, y hay un 404 para /images/hero.jpg. Encuentra la imagen o usa otra."

Nunca escribas una oración que les diga que editen un archivo, instalen algo manualmente o ejecuten un comando que no entienden. Si de verdad hace falta un comando, la oración le pide a Claude que lo ejecute, no a ellos.

Para la categoría **Rebobínalo**, el entregable es distinto: diles que escriban `/rewind` (o presionen Esc dos veces con el cuadro de texto vacío), elijan el punto de control de antes del cambio y luego vuelvan a pedir lo que querían en un paso más pequeño.

### 6. Da la prevención en una línea
Una oración sobre cómo hacer que esto sea menos probable la próxima vez. Normalmente son pasos más pequeños, o un punto de control antes de un cambio grande. Mantenlo en una línea — esto no es una clase.

## Resultado — guárdalo
Crea `~/claude-errors/` si hace falta. Guarda como `~/claude-errors/<date>-<short-slug>.md`, por ejemplo `~/claude-errors/2026-07-30-blank-page.md`.

El archivo contiene: el texto del error palabra por palabra, la categoría, las tres líneas en lenguaje simple, la oración exacta para arreglarlo en un bloque listo para copiar y la prevención en una línea.

Diles la ruta y luego la única siguiente acción: copiar la oración para arreglarlo y pegársela a Claude. Nada más.

Menciona una vez que esta carpeta se convierte en su propio registro de solución de problemas — cuando el mismo error aparezca dentro de tres semanas, ya tendrán la respuesta.

## Ejemplo (entrada → salida)

**Entrada:** "Le pedí a Claude que agregara un formulario de contacto y ahora mi página está toda blanca. Hay un montón de cosas en rojo que dicen `Error: ENOENT: no such file or directory, open './components/ContactForm.jsx'`"

**Salida (guardada en `~/claude-errors/2026-07-30-blank-page.md`):**

**Qué tan grave:** Bloqueado. La página no va a cargar hasta que se resuelva esta única cosa. Es un solo archivo que falta, no un proyecto roto.

**Qué se rompió:** Tu página intentó cargar un archivo de formulario de contacto que no está en tu computadora.

**Por qué:** Claude escribió la línea que usa el formulario pero el archivo del formulario en sí nunca se creó, o se guardó en otro lugar.

**Lo que no es:** No se borró nada. Tu página, tu texto y tus estilos siguen ahí. La pantalla blanca es solo la página negándose a arrancar.

**Pégale esto a Claude:**
```
Mi página ahora está completamente blanca. La terminal dice:
"Error: ENOENT: no such file or directory, open './components/ContactForm.jsx'"
Esto empezó justo después de que agregaste el formulario de contacto. Crea el
archivo que falta para que la página vuelva a cargar y luego muéstrame el formulario.
```

**La próxima vez:** Pide un cambio a la vez, y di "guarda esto como punto de control" cuando algo funcione.

## Notas / casos especiales
- El error que esto evita es que un principiante abandone un proyecto en silencio porque el texto en rojo se sintió como la prueba de que esto no es para él. Aquí el tono importa tanto como la precisión.
- Nunca les digas que editen código, abran un archivo de configuración o ejecuten un comando que no entienden. Si hay que hacerlo, lo hace Claude — ese es el acuerdo.
- Si el texto del error es enorme, encuentra la primera línea que nombra algo real (un archivo, un puerto, un paquete) y trabaja a partir de ella. El resto suele ser el mismo fallo haciendo eco.
- Si no pueden pegar el error, pídeles que describan lo que ven en pantalla. "La página está en blanco" es suficiente para trabajar.
- Si nada de lo que intentan funciona después de dos rondas, deja de depurar y di `/rewind` directamente. Deshacer es más rápido que desenredar, y enseña el instinto correcto.
- Si quieren dejar de tener miedo de que esto pase, pasa a **safety-net**. Si no entienden el archivo que nombra el error, pasa a **explain-this**.
