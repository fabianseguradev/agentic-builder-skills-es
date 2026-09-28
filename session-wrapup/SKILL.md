---
name: session-wrapup
description: Cierra bien una sesión de construcción para que reabrirla mañana tome cinco minutos en lugar de treinta. Resume qué cambió de verdad, qué funciona, qué está a medio terminar, y escribe UNA línea para el primer paso de mañana — luego te propone guardar un punto de control antes de cerrar la laptop. Úsalo cuando el usuario diga "cerrar la sesión", "terminé por esta noche", "fin de la sesión", "registra lo que hicimos", "guarda hasta dónde llegué", "qué hicimos hoy", "voy a parar aquí", "antes de cerrar esto", "cierre de sesión" o escriba /session-wrapup.
---

# Session Wrap-Up — termina la noche para que mañana empiece rápido

Construyes durante 90 minutos, cierras la laptop y vuelves dos noches después sin idea de dónde lo dejaste. Pasas la mitad de la siguiente sesión releyendo archivos y volviendo a explicarte el proyecto. Esa media hora perdida es la razón por la que los proyectos mueren.

Estos son los últimos diez minutos de la noche. Escribe qué cambió, qué funciona, qué está a medio terminar y una sola línea que le dice al tú de mañana exactamente por dónde retomar. Una línea. No una lista de tareas.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Mira qué pasó realmente
No le preguntes al usuario qué cambió — estaba mirando con poca atención y va a reportar de menos. Averígualo tú mismo.

Ejecuta `pwd` para confirmar el proyecto, luego revisa qué cambió: si la carpeta es un repositorio de git, ejecuta `git status` y `git diff --stat`. Si no lo es, lista los archivos y comprueba qué se modificó hoy.

Repasa también esta sesión para ver qué hiciste. Luego dilo en lenguaje simple, de tres a seis líneas, sin jerga: "La página ahora tiene un titular, tres tarjetas y un botón de contacto que funciona. Las fotos siguen siendo marcadores de posición."

Si el usuario empieza la sesión con este skill y no hay historial que leer, hazle una pregunta en su lugar: "¿Qué cambiaste esta noche?"

### 2. Separa lo que funciona de lo que está a medias
Clasifica todo en dos pilas honestas. Sé estricto — esta lista solo sirve si es verdadera.

- **Funciona:** cosas que tú o el usuario de verdad miraron y vieron comportarse correctamente. Si no se abrió ni se comprobó, no va aquí.
- **A medias:** empezado y no terminado, o terminado y no comprobado. Di qué falta en una frase cada uno.

Si algo está a medias y el usuario cree que está terminado, dilo ahora. Descubrirlo mañana cuesta más.

### 3. Anota cualquier cosa que te haya sorprendido
Una o dos líneas, solo si hay algo real: una decisión que se tomó, algo que resultó más difícil de lo esperado, una elección que deberían recordar. Sáltate esto si no pasó nada notable. No lo rellenes.

### 4. Escribe la única línea para mañana
Esta es la línea más valiosa del archivo, así que acierta. Tiene que ser:

- **Un solo movimiento, no una lista.** Si escribes tres cosas, el tú de mañana las lee las tres y no empieza ninguna.
- **Lo bastante específica como para empezar en frío.** "Seguir trabajando en la página" no sirve. "Reemplaza las tres fotos de marcador de posición por reales y compruébalo en un teléfono" es un disparo de salida.
- **Lo bastante pequeña para 75 minutos.**

Escríbela, reléela y pregúntate: ¿podría alguien que olvidó todo empezar solo con esta oración? Si no, reescríbela.

### 5. Propón el punto de control
Antes de que cierren, diles que guarden un punto de control para que el trabajo de esta noche quede a salvo de forma permanente:

Di: "Escribe 'guarda esto como un punto de control' y voy a guardar una instantánea permanente a la que siempre puedes volver."

Si preguntan por qué, una línea: significa que cualquier error futuro se puede deshacer hasta volver exactamente a este estado. Recuérdales también que `/rewind` existe para deshacer cambios dentro de una sesión.

Si no quieren un punto de control, no insistas dos veces. Anota en el registro que no hubo uno.

### 6. Agrega la entrada y cierra bien
Escribe la entrada (formato abajo), diles la ruta y termina la sesión diciendo en voz alta la única línea para mañana. Eso es lo último que deberían leer antes de cerrar la laptop.

## Resultado — guárdalo
Agrega una entrada con fecha al final de `~/build-log.md` (crea el archivo si no existe). Nunca sobrescribas entradas anteriores — este registro es la memoria de todo el proyecto.

```markdown
---

## <YYYY-MM-DD> — <nombre del proyecto>

**Qué cambió**
- <línea en lenguaje simple>
- <línea en lenguaje simple>

**Funciona**
- <cosa que se comprobó y se comporta bien>

**A medias**
- <cosa> — <qué falta>

**Vale la pena recordar**
- <decisión o sorpresa, o se omite esta sección>

**Punto de control:** <guardado / no guardado>

**Mañana, primer paso:**
<Una oración específica.>
```

Diles que la ruta es `~/build-log.md` y da una siguiente acción: "Mañana, abre este archivo primero y lee la última entrada. Luego haz el primer paso y nada más."

## Ejemplo (entrada → salida)
**Entrada:** El usuario pasó 90 minutos en una landing page para un negocio de paseo de perros. Metió el diseño y el texto, el botón de contacto quedó a medio conectar y nunca lo comprobó en un teléfono.

**Salida (agregada a `~/build-log.md`):**
```markdown
---

## 2026-07-30 — paws-page

**Qué cambió**
- La página ahora tiene un titular, una sección corta de "qué hago" y tres tarjetas de servicio con precios.
- Se agregó un botón de contacto debajo de las tarjetas.
- Se cambiaron las fuentes a las que elegiste.

**Funciona**
- La página carga y se lee de arriba a abajo en una laptop. El texto es real, no relleno.
- Los tres precios se muestran correctamente.

**A medias**
- El botón de contacto se ve bien pero todavía no abre nada — necesita que le conectes tu email o tu número de teléfono.
- Nunca se abrió en un teléfono, así que se desconoce cómo se ve el diseño en pantallas pequeñas.

**Vale la pena recordar**
- Decidiste liderar con el nombre del barrio en el titular. Eso es lo que le dio sensación de local, consérvalo.

**Punto de control:** guardado

**Mañana, primer paso:**
Conecta el botón de contacto para que abra un mensaje de texto a tu número, luego abre la página en tu teléfono y dime qué se ve mal.
```

## Notas / casos especiales
- El error que esto evita es la reapertura en frío. Sin un movimiento de una línea para el siguiente paso, los primeros 30 minutos de cada sesión se van en releer en lugar de construir.
- Si la sesión fue un desastre y nada funciona, regístralo con honestidad. "Nada funciona, la página está en blanco, empieza describiendo lo que ves" es un siguiente paso perfectamente válido.
- Nunca escribas una lista de tareas en la línea de mañana. Un movimiento. Las ideas extra van en la lista de "a medias" o en el archivo del plan.
- Si llevan horas y las cosas están empeorando, diles que paren. El registro va a seguir ahí. Construir cansado es de donde viene el desastre.
- Si el proyecto todavía no tiene un plan y se nota, mándalos a **plan-first** para la próxima sesión.
- El domingo, este registro es lo que lee **weekly-review** para ver qué se lanzó de verdad, así que mantén las entradas honestas.
