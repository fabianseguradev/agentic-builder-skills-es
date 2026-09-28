---
name: stuck-unstick
description: Sal del ciclo en el que Claude te sigue dando lo que no es y tú sigues volviendo a pedir. Diagnostica en cuál de las cinco trampas comunes estás — el pedido es demasiado grande, estás describiendo el arreglo en lugar de lo que viste, el chat está contaminado, cambiaste tres cosas a la vez, o estás intentando editar código tú mismo — y luego te da la oración exacta para enviar a continuación. Úsalo cuando el usuario diga "estoy atascado", "Claude me sigue dando lo que no es", "estamos dando vueltas en círculos", "no me está escuchando", "he preguntado cinco veces", "se rompió y ahora está peor", "esto no está funcionando", "sigo teniendo que rehacer esto", "ayuda, estoy dando vueltas" o escriba /stuck-unstick.
---

# Stuck / Unstick — un triaje para dejar de dar vueltas en círculos

Pediste un cambio. Salió mal. Volviste a pedirlo, salió mal de otra forma. Ahora llevas ocho mensajes, la cosa está peor que cuando empezaste, y estás empezando a pensar que eres malo para esto. No lo eres. Estás en una de cinco trampas, y cada una tiene una salida específica.

Este skill encuentra la trampa y te da la oración exacta para enviar a continuación. No arregla tu proyecto. Arregla el ciclo.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Toma la temperatura primero
Antes de diagnosticar nada, di una verdad tranquilizadora: nada está roto para siempre. `/rewind` deshace cambios en esta sesión (Esc dos veces con el cuadro de texto vacío hace lo mismo). Si se guardó un punto de control, todo puede volver a ese estado exacto. No pueden arruinar el proyecto desde aquí.

Luego haz dos preguntas y espera:
1. "¿Qué pediste, con tus propias palabras?"
2. "¿Qué recibiste en su lugar?"

Toma las respuestas al pie de la letra. Todavía no empieces a resolver.

### 2. Diagnostica la trampa
Compara lo que te dijeron con estas cinco. Nombra la trampa en voz alta con palabras simples — los principiantes se sienten mucho mejor en el momento en que el problema tiene un nombre.

**Trampa 1 — el pedido era demasiado grande.**
Señales: el pedido tenía un "y" en el medio, o cubría toda una página, o era un párrafo. Cada intento arregla una parte y rompe otra.
*El movimiento:* divídelo. Elige la pieza más pequeña posible y pide solo eso.

**Trampa 2 — describir el arreglo en lugar del síntoma.**
Señales: están diciendo "cambia el padding", "haz el div más pequeño", "usa flexbox" — instrucciones sobre código en lugar de lo que vieron. Están adivinando una causa y Claude está implementando obedientemente la suposición equivocada.
*El movimiento:* describe lo que VISTE. No lo que crees que lo causó. "En mi teléfono el botón se corta del lado derecho" es cien veces mejor que "arregla el padding".

**Trampa 3 — el chat está contaminado.**
Señales: más de 40 mensajes, varias direcciones abandonadas, Claude volviendo a algo que dejaron hace una hora. Los giros equivocados anteriores siguen en la sala.
*El movimiento:* empieza una sesión nueva con un resumen. El contexto viejo está arrastrando de lado cada respuesta.

**Trampa 4 — cambiaron tres cosas a la vez.**
Señales: pidieron varios cambios juntos, algo se rompió y nadie puede decir cuál cambio lo hizo.
*El movimiento:* deshacer hasta cuando funcionaba, luego cambiar una cosa y mirarla. Luego la siguiente. Más lento se siente más lento y en realidad es más rápido.

**Trampa 5 — intentar editar código a mano.**
Señales: abrieron un archivo, cambiaron algo y ahora está peor o nada carga. O están preguntando qué línea editar.
*El movimiento:* dejar de editar. Cerrar el archivo. Describir el resultado que quieren en lenguaje simple y dejar que Claude haga el cambio. Ellos son el director, no el mecanógrafo.

Si encajan dos trampas, nombra ambas pero elige cuál arreglar primero — normalmente el pedido más grande o el contexto más sucio.

### 3. Devuelve la oración exacta a continuación
Este es el entregable. No expliques el principio y los dejes escribirla — escríbeles la oración, con sus palabras, lista para enviar.

Una buena oración de desatasque tiene cuatro partes:
- **Lo que ves ahora:** "El botón de contacto se corta del lado derecho en mi teléfono."
- **Lo que quieres en su lugar:** "Debería estar completamente en pantalla, con espacio alrededor."
- **La única cosa a cambiar:** "Cambia solo ese botón. No toques nada más de la página."
- **Cómo lo sabremos:** "Luego muéstrame la página para que pueda volver a mirarla."

Dales una oración para enviar, en un bloque listo para copiar. Si la trampa es el contexto contaminado, la oración es en su lugar una apertura de sesión nueva — mira el siguiente paso.

### 4. Si el arreglo es un comienzo nuevo, escribe el relevo
Cuando el diagnóstico es la trampa 3, no digas solo "empieza un chat nuevo". Escribe el párrafo resumen que van a pegar en la sesión nueva para que no pierdan las partes buenas. Incluye:

- Qué es el proyecto, en una oración
- Qué funciona ahora mismo
- Qué está roto, descrito como lo que ven
- Qué ya se intentó y no funcionó, para que no se vuelva a intentar
- La única cosa a hacer a continuación

Luego diles: cierren esta sesión, abran una nueva en la misma carpeta, peguen ese párrafo.

### 5. Fija la expectativa del ciclo
Diles lo que nadie les dijo: de cinco a diez rondas de "describir, mirar, reaccionar" es normal. ESE es el flujo de trabajo. Ir y venir no es evidencia de que están fallando — es evidencia de que están construyendo. Lo que no es normal es ir y venir sin mirar el resultado entre rondas. Miren cada vez.

### 6. Da permiso explícito para reiniciar
Termina con esto, claramente: si sigue dando vueltas en círculos después de dos intentos más, usen `/rewind` para volver atrás y empezar de nuevo la pieza desde el último buen estado. Reiniciar una pieza de trabajo de 40 minutos es barato. Pelear contra una dirección rota durante tres noches no lo es. Los principiantes creen que reiniciar significa fallar. Es el movimiento más rápido que tienen disponible.

## Resultado — guárdalo
Escribe el diagnóstico y la siguiente oración en `~/build-log.md` como una entrada de "atascado" con fecha (crea el archivo si no existe), para que el patrón sea visible con el tiempo:

```markdown
---

## <YYYY-MM-DD> — atascado: <nombre del proyecto>

**Qué pediste:** <sus palabras>
**Qué recibiste:** <sus palabras>
**Trampa:** <nombre de la trampa, una línea de por qué>

**Manda esto a continuación:**
<la oración exacta>

**Si sigue atascado después de dos intentos:** /rewind y reinicia esta pieza desde el último buen estado.
```

Diles la ruta, y da una siguiente acción: "Copia la oración de arriba y mándala como tu próximo mensaje."

## Ejemplo (entrada → salida)
**Entrada:** "He pedido cuatro veces que la página se vea bien en mi teléfono y sigue cambiando otras cosas. Ahora el encabezado también está roto y no sé qué pasó."

**Salida (guardada en `~/build-log.md`):**
```markdown
---

## 2026-07-30 — atascado: paws-page

**Qué pediste:** "que se vea bien en mi teléfono"
**Qué recibiste:** el diseño del teléfono sigue mal, y ahora el encabezado también está roto
**Trampa:** El pedido era demasiado grande. "Que se vea bien en mi teléfono" cubre toda la página, así que cada intento mueve varias cosas y rompe algo nuevo.

**Manda esto a continuación:**
En mi teléfono, las tres tarjetas de servicio están apretadas lado a lado y el texto es demasiado pequeño para leer. Quiero que estén apiladas una encima de la otra, a todo el ancho, con texto legible. Cambia solo las tarjetas — deja en paz el encabezado y el botón. Luego muéstrame la página para que pueda mirar.

**Si sigue atascado después de dos intentos:** /rewind y reinicia esta pieza desde el último buen estado.
```

## Notas / casos especiales
- Si no pueden decir qué vieron, pídeles que te lean la pantalla en voz alta. "Está roto" no es un síntoma; "la página está en blanco y toda blanca" sí lo es.
- Si llevan más de una hora en esto y están frustrados, diles que paren por esta noche y ejecuten **session-wrapup**. Depurar cansado hace más desastre.
- Si la misma trampa aparece tres veces entre sesiones, el verdadero arreglo está más arriba: una regla en **claude-md-builder**, o un alcance más pequeño desde **plan-first**.
- Nunca les digas que abran un archivo y cambien una línea. Esa es la trampa 5 y empeora las cosas.
- Si el proyecto de verdad no tiene un último buen estado al que hacer rewind, dilo y reconstruye la pieza rota a partir de una descripción simple. No finjas que existe un punto de control.
