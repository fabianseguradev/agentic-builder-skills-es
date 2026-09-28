---
name: rewrite-plain
description: Reescribe cualquier cosa en un lenguaje simple y directo que una persona ocupada entiende en la primera lectura. Elimina la jerga, los rodeos, la voz pasiva, las aperturas de calentamiento y las palabras corporativas que no significan nada — mientras mantiene tu significado y cada dato exactamente como estaban. Muestra un breve antes/después para que empieces a notar el patrón tú mismo. Funciona en emails, posts, bios, páginas de ventas, documentos, lo que sea. Úsalo cuando el usuario diga "haz esto más simple", "esto suena corporativo", "reescribe esto", "en lenguaje simple", "limpia esto", "haz esto más claro", "esto tiene sentido", "demasiado verboso", "simplifícalo", "ajústalo" o /rewrite-plain.
---

# Rewrite Plain — dilo para que pegue a la primera

La escritura poco clara no suele ser un problema de vocabulario. Normalmente es alguien cubriéndose, o escondiéndose, o calentando motores durante tres oraciones antes de decir algo. Este skill quita eso y deja el significado intacto. Es una pasada de claridad, no una reescritura de tu argumento — los mismos hechos, la misma postura, las mismas afirmaciones, dichas para que una persona ocupada las entienda en una lectura.

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia — yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## Pasos

### 1. Consigue el texto y una pieza de contexto
Toma el texto (pegado, o una ruta de archivo). Haz solo una pregunta: **"¿Quién lee esto, y qué quieres que hagan después?"** Si ya lo dijeron, sáltatela.

Esa respuesta define cuánto puedes recortar. Una página de ventas para desconocidos y una nota para tu contador reciben un trato distinto.

### 2. Encuentra el punto
Léelo y escribe, para ti mismo, la única oración que es el punto real. Luego revisa dónde está en el original — normalmente en el párrafo dos o tres, enterrado detrás del preámbulo.

Si no puedes encontrar un punto, detente y dilo: "No logro entender qué me estás pidiendo aquí. ¿Cuál es la única cosa que quieres que sepan?" Una reescritura clara de una idea poco clara sigue siendo poco clara.

### 3. Recorta las siete cosas
Recorre el texto y elimina:

1. **Aperturas de calentamiento.** "Espero que esto te encuentre bien." "En el mundo de hoy." "Como sabrás." "Quería contactarte para." Bórralas y empieza en la primera oración real.
2. **Rodeos.** "solo", "como que", "medio que", "creo que tal vez", "quizás", "puede que esté equivocado pero", "¿tiene sentido esto?". Di la cosa. Conserva un rodeo solo cuando la incertidumbre es real e importa.
3. **Voz pasiva que esconde al actor.** "Se cometieron errores" se convierte en "me equivoqué de fecha". La pasiva está bien cuando el actor de verdad no importa; no está bien cuando está evadiendo.
4. **Palabras corporativas que no significan nada.** apalancar, utilizar, sinergia, holístico, robusto, fluido, empoderar, desbloquear, elevar, optimizar, de primer nivel, valor agregado, soluciones, de cara al futuro, retomar contacto, ponernos en contacto, profundizar, al final del día, mover la aguja.
5. **Nominalizaciones** — verbos convertidos en sustantivos. "tomar una decisión" es "decidir". "brindar asistencia" es "ayudar". "tiene un requerimiento de" es "necesita".
6. **Palabras largas haciendo el trabajo de una corta.** utilizar/usar, comenzar/empezar, finalizar/terminar, con anterioridad a/antes, con el fin de/para, adicional/más, suficiente/bastante, aproximadamente/como, actualmente/ahora.
7. **Repeticiones.** El mismo punto dicho dos veces con distinta ropa. Conserva el mejor.

### 4. Reconstrúyelo
Ahora vuelve a armarlo:

- **Punto primero.** Lo que necesitan saber va en las primeras dos líneas.
- **Una idea por oración.** Corta cualquier oración de más de unas 25 palabras en su unión natural.
- **Párrafos cortos.** De una a tres líneas. El espacio en blanco se lee bien.
- **Concreto antes que abstracto.** "£1,800, cinco semanas de retraso" le gana a "un saldo pendiente". Nombres, números, fechas, objetos.
- **Verbos antes que sustantivos.** "Decidimos" le gana a "se llegó a una decisión".
- **Conserva sus palabras reales.** Si dijeron algo bien en el original — una frase que suena a una persona — consérvala exactamente. No suavices una buena línea hasta volverla insulsa.
- **Léelo en voz alta en tu cabeza.** Si te quedarías sin aire o tropezarías, córtalo ahí.

Apunta a un 30–50% más corto. Di el conteo de palabras final y el original.

### 5. Protege el significado
Antes de mostrarlo, compara la reescritura con el original línea por línea:

- Cada dato, número, fecha, nombre y afirmación sobrevive sin cambios.
- No apareció ninguna afirmación, promesa o número nuevo. Ninguno.
- La postura no se suavizó ni se endureció. Si cubrieron algo deliberadamente por ser genuinamente incierto, ese rodeo se queda.
- Nada legalmente o fácticamente importante se cortó como "verboso" — las salvedades en contratos y descargos de responsabilidad suelen estar ahí por una razón.

Si cortar una frase cambiaría el significado, consérvala y di por qué en una línea.

### 6. Muestra el patrón
Debajo de la reescritura, muestra **de tres a cinco pares de antes/después** de su propio texto — una línea cada uno. Elige los que más enseñan, y nombra el movimiento en dos o tres palabras.

> **Antes:** "Queríamos contactarte con el fin de brindarte una actualización con respecto al estado actual del proyecto."
> **Después:** "Aquí está en qué va el proyecto."
> *Corte: calentamiento + nominalizaciones.*

Esta es la parte que los hace mejores la próxima vez. No la saltes, y no hagas más de cinco — deja de enseñar y empieza a sermonear.

## Resultado — guárdalo
Escribe en `~/rewrites/<short-slug>-<YYYY-MM-DD>.md` (crea `~/rewrites/` si hace falta):

```
# Reescritura — <qué es>
## La reescritura
<limpia, lista para pegar, nada más en esta sección>
## Conteo de palabras
## Qué cambié y por qué
## Antes / después — los patrones
## Original
```

Mantén el original al final para que nada se pierda. Dile al usuario la ruta, y pega la reescritura limpia directamente en tu respuesta para que pueda copiarla sin abrir nada.

## Ejemplo (entrada → salida)
**Entrada:** Una bio para un sitio web: "Con más de una década de experiencia en la industria, apalanco un enfoque holístico basado en datos para empoderar a empresas de todos los tamaños a desbloquear todo su potencial mediante la utilización de soluciones digitales de primer nivel adaptadas a sus necesidades únicas."

**Salida (guardada en `~/rewrites/bio-2026-07-30.md`):**

> **La reescritura:** "Llevo diez años ayudando a pequeñas empresas a arreglar sus sitios web y conseguir más clientes con ellos. Sobre todo tiendas, oficios y estudios de una sola persona."
>
> **Conteo de palabras:** 44 → 26.
>
> **Antes / después:**
> - **Antes:** "apalanco un enfoque holístico basado en datos" → **Después:** cortado por completo. *No dice nada, y cortarlo no perdió nada.*
> - **Antes:** "empresas de todos los tamaños" → **Después:** "pequeñas empresas. Sobre todo tiendas, oficios y estudios de una sola persona." *"Todos los tamaños" hace que nadie se imagine a sí mismo. Nombrar tres tipos hace que tres tipos se reconozcan.*
> - **Antes:** "mediante la utilización de soluciones digitales de primer nivel" → **Después:** "arreglar sus sitios web". *Di el trabajo real.*
> - **Antes:** "más de una década de experiencia" → **Después:** "diez años". *El mismo dato, una máscara menos.*

## Notas / casos especiales
- El error de principiante que esto evita: escribir para sonar profesional y terminar sonando a nadie. Simple no es poco profesional. Simple es seguro.
- Esto es una pasada de claridad. Nunca cambies su argumento, suavices un "no", refuerces una afirmación ni agregues un número que no te dieron. Si crees que el argumento en sí está mal, dilo por separado — no lo arregles en silencio en la reescritura.
- Si el texto ya está claro, dilo y haz tres recortes pequeños en lugar de fabricar una reescritura. No todo necesita cirugía.
- Los términos técnicos se quedan cuando el lector los conoce. Simple significa "sin palabras que escondan el significado", no "sin palabras específicas". Cortar el término correcto por uno vago lo empeora.
- Redacción legal, médica o contractual: señala lo que cortarías en lugar de cortarlo, y sugiere una revisión profesional.
- Si necesitan que se escriba todo el email en lugar de que se ordene, usa **email-writer**.
