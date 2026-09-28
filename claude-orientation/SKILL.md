---
name: claude-orientation
description: Te dice exactamente qué construir primero con Claude Code y te da el único siguiente paso de esta noche en lugar de un montón de ideas. Determina en qué punto estás del arco de principiante de 9 etapas, elige UN proyecto y guarda una hoja de ruta de 30 días que puedes volver a abrir cada noche. Úsalo cuando el usuario diga "acabo de instalar Claude Code", "¿y ahora qué?", "qué debería construir primero", "por dónde empiezo", "no sé qué hacer con esto", "tengo demasiadas ideas", "cuál es mi primer proyecto", "ayúdame a empezar", "/claude-orientation", o cuando alguien claramente salta entre proyectos y no termina ninguno.
---

# Claude Orientation — un proyecto, un siguiente paso

La mayoría de la gente instala Claude Code, mira tres videos, empieza cinco proyectos y termina cero. No es un problema de disciplina. Es un problema de orden — nadie les dijo en qué orden hacer las cosas. Este skill encuentra dónde estás realmente, elige el único siguiente proyecto y escribe el paso de esta noche, en una línea, en un archivo que vuelves a abrir en cada sesión.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Ubícalos en el arco
Hay un arco de principiante de 9 etapas. Cada etapa supone la anterior. Léelas en voz alta de forma simple y luego pregunta cuál fue la última que terminaron:

1. **Instalación** — Claude Code está abierto y ya hablaste con él una vez.
2. **Memoria** — tienes un `CLAUDE.md` para que Claude recuerde quién eres entre sesiones.
3. **Sitio web** — una página en línea sobre ti, en internet, con una URL.
4. **Landing page** — una página con una acción clara que un visitante puede tomar.
5. **Skills** — hiciste un skill propio que realiza una tarea repetitiva por ti.
6. **Juego** — una cosa interactiva pequeña, para demostrar que puedes construir estado y lógica.
7. **Agentes** — algo que ejecuta un trabajo por ti sin que tengas que vigilar cada paso.
8. **Contenido** — conviertes lo que construyes en posts, para que construir se acumule.
9. **Distribución** — pones la cosa frente a personas reales a propósito.

Haz exactamente dos preguntas:
- "¿Cuáles de estas nueve has terminado de verdad — no mirado, terminado?"
- "¿Qué has intentado construir hasta ahora, aunque no haya llegado a nada?"

Si no pueden responder la primera, asume la Etapa 1.

### 2. Fija la etapa y niégate a saltarla
Su etapa es **la primera que NO han terminado.** Dilo claramente: "Estás en la Etapa N."

Si quieren adelantarse — un agente en la Etapa 2, una app en la Etapa 3 — no discutas sobre la ambición. Di en una línea lo que les da la etapa que se saltan ("sin un CLAUDE.md te vuelves a explicar cada noche") y pon la gran idea en una lista de Más Adelante en la hoja de ruta para que no se pierda. Conservan la ambición, solo que no empiezan por ahí.

### 3. Elimina las ideas de más
Pregunta: "Enumera todos los proyectos en los que estás pensando ahora mismo." Toma la lista y redúcela a uno.

Elige al sobreviviente con estas pruebas, en orden:
- **Encaje con la etapa** — ¿coincide con la etapa del Paso 2?
- **Terminable en una semana** — ¿se puede hacer en cinco noches de 90 minutos? Si no, recorta su alcance hasta que se pueda.
- **Audiencia real** — ¿hay una persona específica a la que podrían enviárselo cuando esté listo? Nombra a esa persona.
- **Su propia necesidad** — ¿de verdad quieren que exista?

Todo lo que pierde va a una sección de **Estacionamiento**. No se borra nada. Ese es el trato que hace que la gente acepte el recorte.

Declara al ganador en una oración: "Estás construyendo ___ , para ___ , listo cuando ___ ."

### 4. Recórtalo a una primera versión que salga esta semana
Los principiantes planifican el alcance como una empresa. Encógelo. Aplica la **Regla de Un Solo Trabajo**: el proyecto hace una cosa. Una página, una acción, un resultado. Si tiene dos funciones, quita una y ponla en el Estacionamiento.

Escribe una línea de Listo-Cuando que se pueda comprobar mirando, no sintiendo: "un desconocido puede abrir este link en su celular y reservar una llamada" le gana a "el sitio está terminado".

Recuérdales: **feo-pero-en-línea le gana a bonito-pero-local.** Que la primera versión sea sencilla es lo correcto.

### 5. Divide la semana en cinco noches
Trabajan en horas robadas, unos 90 minutos. Escribe cinco noches, cada una con UN paso específico. Cada noche sigue la misma forma: 5 minutos para reabrir y leer la última nota, 75 minutos en el único paso, 10 minutos para guardar un punto de control y escribir la línea de mañana.

Las noches deberían ir escalando: poner algo en pantalla, hacerlo real, hacerlo bueno, ponerlo en línea, enviárselo a un ser humano. La Noche 5 siempre es "envíaselo a una persona real" — lanzarlo a alguien es la repetición que cuenta.

### 6. Escribe el único siguiente paso de esta noche
Una línea, una oración, que empiece con un verbo, se pueda hacer en 90 minutos y sea lo bastante específica como para que no tengan que pensar cuando se sienten. No "trabajar en el sitio". Más bien: "Pídele a Claude que construya un sitio de una página sobre mí con mi nombre, una oración sobre lo que hago y un botón que abra mi email."

Incluye exactamente lo primero que tienen que pegar en Claude. Dales las palabras.

### 7. Esboza el arco de 30 días
Cuatro semanas, una línea cada una, llevándolos hacia adelante a través de las etapas. Mantenlo flexible — es una dirección, no un contrato. La Semana 1 es el proyecto del Paso 3. Las Semanas 2-4 son las siguientes etapas en orden.

## Resultado — guárdalo
Escribe todo en `~/claude-roadmap.md`. Sobrescríbelo si ya existe, pero primero léelo y trae todo lo que hubiera en el Estacionamiento anterior.

El archivo contiene, en este orden:
- **Dónde estás** — el número y el nombre de la etapa, una línea sobre por qué.
- **El único proyecto** — la oración del Paso 3, más la línea de Listo-Cuando.
- **El siguiente paso de esta noche** — una oración, más el texto exacto para pegar en Claude.
- **Esta semana, cinco noches** — cinco pasos de una línea.
- **El arco de 30 días** — cuatro líneas, una por semana.
- **Estacionamiento** — cada idea que se recortó, para que nada se sienta perdido.

Diles la ruta. Diles una cosa: "Abre este archivo al inicio de cada sesión. Haz el siguiente paso. Luego reescribe la línea del siguiente paso antes de cerrar la laptop."

## Ejemplo (entrada → salida)

**Entrada:** "Instalé Claude Code la semana pasada. Quiero construir una app para mi negocio de coaching, un sitio para un newsletter, una extensión de Chrome y quizás un agente de IA que agende llamadas. No he terminado nada."

**Salida (guardada en `~/claude-roadmap.md`):**
```
DÓNDE ESTÁS
Etapa 2 — Memoria. Claude Code está instalado pero no tienes un CLAUDE.md,
así que cada sesión empieza desde cero.

EL ÚNICO PROYECTO
Estás construyendo un sitio de una página sobre tu coaching, para un cliente
que no deja de preguntar "dónde puedo leer sobre lo que haces", listo cuando
ese cliente pueda abrir el link en su celular y ver tu oferta y una forma de
contactarte.

EL SIGUIENTE PASO DE ESTA NOCHE
Configura tu CLAUDE.md para que Claude sepa quién eres y luego empieza la página.
Pega esto: "Crea un CLAUDE.md en mi carpeta de inicio con mi nombre, lo que hago,
a quién ayudo y cómo me gusta que me hables. Hazme las preguntas que necesites."

ESTA SEMANA
Noche 1 — CLAUDE.md, y luego poner cualquier versión de la página en pantalla.
Noche 2 — Palabras reales. Tu oferta en lenguaje simple, sin texto de relleno.
Noche 3 — Haz que se vea como tú. Un color de acento, dos fuentes.
Noche 4 — Ponla en línea y consigue una URL.
Noche 5 — Mándale la URL a ese cliente. Pregúntale qué es confuso.

ARCO DE 30 DÍAS
Semana 1 — Sitio de una página en línea.
Semana 2 — Convertirlo en una landing page con una acción clara.
Semana 3 — Construir tu primer skill propio para una tarea que repites.
Semana 4 — Publicar lo que construiste. Empezar la Etapa 8.

ESTACIONAMIENTO
App de coaching. Sitio del newsletter. Extensión de Chrome. Agente para agendar
llamadas. Todas siguen siendo tuyas. Ninguna es para esta noche.
```

## Notas / casos especiales
- El error que esto evita es el síndrome del objeto brillante. Si se resisten a recortar a un solo proyecto, no debatas — señala el Estacionamiento y sigue adelante. La lista es la concesión.
- Si de verdad han terminado varias etapas, no los dejes en la Etapa 1 por las dudas. Pregunta qué lanzaron y dónde está. La evidencia fija la etapa, no la confianza.
- Si dicen "no tengo ideas", no hagas una lluvia de diez. Pregunta qué hacen todo el día y qué parte de eso es molesta. El primer proyecto sale de ahí en dos preguntas.
- Si la entrada es escasa — un "¿y ahora qué?" de una línea — asume la Etapa 2, elige el sitio de una página y escribe la hoja de ruta de todos modos. Un plan por defecto le gana a una entrevista que van a abandonar.
- Una vez que tengan el proyecto elegido y quieran el prompt para ejecutarlo de verdad, pasa a **brief-builder**. Si les da miedo romper algo, pasa a **safety-net** antes de que empiecen.
