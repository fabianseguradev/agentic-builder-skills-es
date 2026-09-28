---
name: safety-net
description: Configura tus dos sistemas de deshacer para que puedas experimentar sin preocuparte por arruinar tu proyecto — /rewind para deshacer al instante y puntos de control de Git para guardados permanentes. Te guía para hacer tu primer punto de control en el proyecto que tienes abierto, y luego guarda una hoja de referencia de una página con los movimientos exactos de recuperación para "lo rompí", "vuelve un paso atrás" y "vuelve a esta mañana". Úsalo cuando el usuario diga "tengo miedo de romper algo", "cómo deshago esto", "puedo volver atrás", "rompí mi proyecto", "cómo guardo mi trabajo", "qué es un checkpoint", "cómo funciona rewind", "hay un deshacer", "quiero probar algo arriesgado" o "/safety-net".
---

# Safety Net — dos formas de deshacer, para que puedas experimentar

Los principiantes construyen con timidez porque creen que un mal prompt arruina todo. No es así. Tienes dos sistemas de deshacer separados, y una vez configurados puedes intentar cosas que de otro modo evitarías. Este skill explica ambos, hace tu primer punto de control real en tu proyecto actual y te deja una hoja de referencia que mantienes abierta.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Di lo que necesitan escuchar
Ábrelo con esto, claramente: "En realidad no puedes romper nada. Hay dos botones de deshacer, y al final de esto vas a tener ambos funcionando en este proyecto."

Luego nombra los dos, y nombra la diferencia — esta es la parte con la que todos se confunden:

- **`/rewind`** — automático, instantáneo, de corto plazo. Claude Code toma una instantánea antes de cada cambio que hace. Tú no configuraste esto y no tienes que hacerlo. Es para "lo último que hice lo empeoró."
- **Puntos de control de Git** — manuales, permanentes, de largo plazo. Dices "guarda esto como un punto de control" y ese estado exacto del proyecto queda guardado para siempre con un nombre. Es para "llévame de vuelta a como estaba el martes cuando funcionaba."

Una línea para fijarlo: **rewind deshace movimientos, los puntos de control guardan días.**

### 2. Enseña bien el /rewind
Cubre exactamente esto, nada más:
- Escribe `/rewind` en Claude Code. Obtienes una lista de puntos de control recientes.
- Más rápido: presiona **Esc dos veces** con el cuadro de texto vacío. Lo mismo.
- Elige el punto de antes de que las cosas salieran mal. Tus archivos vuelven a ese estado.
- Es automático — sucede antes de cada cambio, lo pidas o no.
- Lo que no hace: es para trabajo reciente en esta sesión, no para volver días atrás. Para eso están los puntos de control.

Luego haz que lo prueben de verdad una vez. Di: "Pídele a Claude que haga un cambio pequeño y sin sentido — cambia un encabezado a la palabra BANANA. Mira cómo queda. Luego escribe `/rewind` y vuélvelo a como estaba." Hacerlo una vez elimina el miedo de forma permanente. Leerlo no.

### 3. Comprueba si este proyecto tiene Git
Pregunta en qué proyecto están trabajando y consigue la ruta de la carpeta. Comprueba si ya es un repositorio de Git — busca una carpeta `.git` en él.

No expliques Git como un sistema de control de versiones. Explícalo como: "una forma de guardar una instantánea permanente de todo el proyecto con un nombre, para que siempre puedas volver a ella."

Si no está configurado, hazlo tú por ellos. Ellos dicen la palabra, tú lo ejecutas. Nunca le des a un principiante una lista de comandos de Git para escribir.

### 4. Haz su primer punto de control ahora mismo
Esta es la parte que tiene que pasar de verdad, no solo describirse.

Haz que le digan a Claude: **"Guarda esto como un punto de control llamado 'versión funcionando antes de empezar a experimentar'."**

Tú haces el resto. Luego confirma en voz alta lo que acaba de pasar: "Ese estado de tu proyecto ahora está guardado de forma permanente. Hagas lo que hagas después, puedes volver exactamente a esto."

Esa oración es todo el punto del skill.

### 5. Fija el hábito del punto de control
Dales los tres momentos para hacer uno. Tres, no diez:
- **Cuando algo funciona.** El momento en que la página carga bien o la función hace lo que debe. Antes de volver a tocarlo.
- **Antes de algo arriesgado.** Un rediseño grande, una función nueva, cualquier cosa de la que no estén seguros.
- **Al final de cada sesión.** Parte de cerrar la laptop — los últimos 10 minutos de una noche de 90 minutos son punto de control más el siguiente paso de mañana en una línea.

Diles cómo nombrar los puntos de control: dicen en qué estado está el proyecto, no lo que hicieron. "página de inicio funcionando en móvil" le gana a "cambios."

### 6. Escribe los tres movimientos de recuperación
Estas son las tres situaciones en las que realmente van a estar. Escríbelos como guiones para leer en voz alta.

**"Lo rompí y no sé cómo."**
No depures. Escribe `/rewind`, o presiona Esc dos veces. Elige el punto de antes de que se rompiera. Luego vuelve a pedir lo que querías en un paso más pequeño.

**"Vuelve un paso atrás."**
Escribe `/rewind`, elige el punto de control más reciente. O dile a Claude: "Deshaz el último cambio que hiciste."

**"Vuelve a esta mañana / a cuando funcionaba."**
Dile a Claude: "Muéstrame mis puntos de control de hoy." Elige el que corresponda por nombre. Luego: "Lleva el proyecto de vuelta al punto de control llamado ___." Rewind no llega tan lejos — para eso están los puntos de control.

Agrega la salida de emergencia: **"Quiero recuperar la versión vieja pero también quiero conservar lo que hice desde entonces."** Dile a Claude: "Guarda lo que tengo ahora como un punto de control, y luego llévame de vuelta a ___." Nada se pierde.

## Resultado — guárdalo
Escribe en `~/claude-safety-net.md`. Una página, no más — esto es una hoja de referencia, no un manual.

Contiene: la diferencia de una línea entre los dos sistemas, los movimientos de `/rewind` incluido Esc-Esc, la oración exacta para hacer un punto de control, los tres momentos para hacer uno, los tres guiones de recuperación palabra por palabra, la salida de emergencia para conservar ambos y el nombre y la fecha del primer punto de control que acaban de hacer.

Diles la ruta, y luego la única acción: mantener este archivo abierto en una pestaña mientras construyen. Diles también la verdad: ahora que ambos deshacer funcionan, lo correcto es ir a probar algo que antes les daba demasiado nervio intentar.

## Ejemplo (entrada → salida)

**Entrada:** "Estoy trabajando en el sitio de mi portafolio y quiero probar un diseño completamente distinto pero me da miedo perder la versión que funciona."

**Salida (guardada en `~/claude-safety-net.md`):**
```
TUS DOS DESHACER
Rewind deshace movimientos. Los puntos de control guardan días.

REWIND — instantáneo, automático
Escribe /rewind, o presiona Esc dos veces con el cuadro de texto vacío.
Elige el punto de antes de que saliera mal. Los archivos vuelven a ese estado.
Solo para trabajo reciente, no para volver días atrás.

PUNTO DE CONTROL — permanente, lo pides tú
Di: "Guarda esto como un punto de control llamado '<en qué estado está>'."
Haz uno cuando algo funcione, antes de algo arriesgado y al final de
cada sesión.

TU PRIMER PUNTO DE CONTROL
"portafolio funcionando antes del experimento de diseño" — guardado 2026-07-30.
Siempre puedes volver exactamente a esto.

SI LO ROMPÍ
No depures. /rewind, elige el punto de antes de que se rompiera, vuelve a
pedirlo más pequeño.

VUELVE UN PASO ATRÁS
/rewind y elige el más reciente. O: "Deshaz el último cambio que hiciste."

VUELVE A CUANDO FUNCIONABA
"Muéstrame mis puntos de control de hoy."
"Lleva el proyecto de vuelta al punto de control llamado ___."

CONSERVA AMBAS VERSIONES
"Guarda lo que tengo ahora como un punto de control, y luego llévame de
vuelta a ___."
```

Siguiente acción: ve a probar el diseño nuevo. El viejo está guardado.

## Notas / casos especiales
- El error que esto evita es construir con timidez — principiantes que evitan la versión interesante porque están cuidando la que funciona. Todo el punto del punto de control es dar permiso para experimentar.
- Haz que de verdad hagan la prueba de rewind en el Paso 2 y de verdad hagan el punto de control en el Paso 4. Un skill que solo describe redes de seguridad no crea la sensación de tener una.
- Nunca les des comandos crudos de Git. Ellos dicen la oración, Claude la ejecuta. Si quieren aprender Git de verdad más adelante, eso es otro día.
- Si el proyecto todavía no es un repositorio de Git, configúralo sin hacer un gran asunto de ello. Es un paso, no cuesta nada y toma 10 segundos.
- Si ya rompieron algo ahora mismo, haz primero el Paso 6 y configura el resto después. Apaga el incendio y luego instala la alarma.
- Si están mirando un error y no saben si hacer rewind, pasa a **error-decoder** — clasifica los errores en ignorar, arreglar o rebobinar.
