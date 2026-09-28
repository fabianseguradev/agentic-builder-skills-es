---
name: content-prompt
description: Genera una única pregunta que invite a pensar para que el usuario la responda frente a cámara como contenido de formato corto (TikTok, Reels, YouTube Shorts o cualquier video improvisado), más 5 opciones de gancho y textos en pantalla. Úsalo siempre que el usuario pida "ideas de contenido", "de qué debería hablar", "dame una pregunta para responder", "dame un disparador", "ideas de formato corto", "qué está en tendencia de lo que pueda hablar", "necesito inspiración para contenido" o escriba /content-prompt. Actívalo siempre que el usuario quiera algo sobre lo que improvisar para un video rápido — incluso un casual "dame algo de qué hablar" o "de qué debería tratar mi próximo video".
---

# Content Prompt Generator

**El propósito de estos videos:** ayudar al usuario a contar historias reales de su propia vida y experiencia que construyan autenticidad, nutran a la audiencia y compartan sabiduría ganada a pulso. Una conversación en tendencia es el *punto de entrada* — la historia real del usuario es el *contenido*. No comentarios de noticias. No consejos genéricos. Su experiencia real, sacada a la luz por una pregunta que vale la pena responder.

**Nivel del embudo: ALCANCE.** Piezas de descubrimiento para audiencia fría. Un golpe de valor, un CTA para seguir. Sin oferta directa, sin links.

## Personalización
Este skill trabaja con *tu* voz, a partir de *tu* historia y *tu* audiencia. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nicho, tu audiencia, tu oferta y un par de momentos reales de tu trayectoria — yo lo creo).
- La semilla de la historia de cada disparador tiene que salir de algo que el usuario vivió de verdad. Si la Prueba/Transformación del perfil es escasa, pídele un momento real (un error, un punto de inflexión, un resultado sorprendente) y guárdalo en el perfil.
- Nunca inventes datos, resultados ni historias sobre el usuario — usa solo lo que está en el perfil, o pregunta.

---

## Paso 1: Carga el contexto

Lee `~/.claude/brand-profile.md`. Extrae:
- **Audiencia + Dolor principal** — a quién le hablas y en qué están atascados
- **Transformación + Prueba** — los momentos reales de la trayectoria del usuario de los que puedes sacar una historia
- **Tono + Palabras a evitar** — cómo debería sonar

Lo que buscas: un momento de la historia del usuario que se corresponda directamente con lo que su audiencia está viviendo ahora mismo.

---

## Paso 2: Elige una categoría + encuentra la tensión viva

**Selecciona al azar uno de los cuatro tipos de categoría de abajo**, adaptado al nicho del usuario. Varía entre ejecuciones — no caigas siempre en el mismo.

- **Categoría A — Visibilidad / Marca personal:** el experto invisible que no consigue tracción a pesar de tener habilidad real. Territorio de historias: publicar y abandonar, un hito de audiencia, construir un sistema vs. matarse trabajando, el momento en que algo hizo clic.
- **Categoría B — Ganar dinero:** la persona con una habilidad que no logra convertirla en ingresos constantes. Territorio de historias: confianza al poner precio, el primer cliente, la brecha entre "lo construí" y "alguien me pagó por ello", vender sin una gran audiencia.
- **Categoría C — Herramienta nueva / Lo que acaba de salir:** el adoptante temprano que quiere mantenerse adelante. Territorio de historias: la experiencia real y de primera mano del usuario probando una herramienta nueva en su campo — qué lo sorprendió, qué se rompió, qué funcionó de verdad vs. la demo.
- **Categoría D — Sistemas / Hacer más con menos:** el operador que se ahoga en trabajo manual. Territorio de historias: reemplazar horas manuales con un sistema, el momento en que dejó de hacerlo a mano, el flujo de trabajo que lo cambió todo.

**Opcional — encuentra la tensión viva:** si el usuario quiere algo oportuno, haz 1-2 búsquedas web de un debate activo o un lanzamiento reciente en su nicho (p. ej. `"[campo del usuario] [frustración común]" reddit 2026`, o `"[herramienta nueva de su campo]" honest review 2026`). No buscas noticias — buscas **fricción activa que el usuario haya vivido personalmente**.

La pregunta que hay que hacerse: *¿hay un momento en la historia del usuario — una decisión, un error que corrigió, una creencia que tuvo que desaprender — que hable directamente de esta tensión?* Si sí, ese es el disparador. Si no, elige otra tensión que sí conecte con una experiencia real.

---

## Paso 3: Encuentra la semilla de la historia

Antes de elegir la pregunta, identifica la **experiencia específica de la vida del usuario** de la que saldría el video. Tiene que ser real — algo que vivió, que esté en el perfil, no algo inventado.

Categorías de historias de las que sacar:
- Un error que cometió y lo que le costó
- Un momento en que casi abandona o cambia de rumbo
- Una creencia que tenía y resultó ser falsa
- Un resultado que lo sorprendió (mejor o peor de lo esperado)
- Algo que dijo un cliente y que cambió su forma de trabajar
- Una decisión que daba miedo pero salió bien
- Algo que hizo distinto a todos los demás — y por qué

La semilla de la historia es el corazón del video. La pregunta es solo la puerta que la abre.

---

## Paso 4: Fija la pregunta

Formula una pregunta que:
- La audiencia se hace en silencio pero no sabe cómo articular
- Abra la puerta a la historia específica del usuario (no a consejos genéricos)
- Cree una brecha: el espectador asume una cosa, la respuesta del usuario la da vuelta
- Se sienta como la primera línea de un TikTok — directa, no académica

Mejores aperturas: "¿Es...", "¿Por qué...", "¿Y si...", "¿Acaso...", "¿Estás..."

---

## Paso 5: Genera 5 ganchos + textos en pantalla

Relaciona la pregunta con un deseo central (Dinero / Tiempo / Salud / Estatus) y luego genera un gancho por variación:

1. **Sobre Mí** — "[Hice X] y esto es lo que pasó"
2. **Si Yo** — "Si empezara de nuevo, [haría Y]"
3. **A Ti** — "Si estás [haciendo X], te estás [perdiendo Y]"
4. **¿Se Puede?** — "¿Es posible [X] sin [Y]?"
5. **Él/Ella Acaba de** — "[Alguien] acaba de [hacer X]. Esto es lo que descubrió."

Para cada gancho:
- Nivel de lectura de quinto grado — corto, sin jerga
- Debe incluir como mínimo: Sujeto + Acción + Objetivo
- Escrito en el Tono del usuario, respetando las Palabras a evitar

**Para cada gancho, escribe también un texto en pantalla.**

El gancho hablado y el texto en pantalla se reproducen al mismo tiempo — el espectador escucha uno mientras lee el otro. Cada uno tiene que sostenerse solo Y decir algo distinto. El texto en pantalla nunca es un subtítulo, una etiqueta ni un resumen del gancho hablado.

**Escribe primero el gancho hablado.** Un gancho completo y autónomo — funciona sin ningún contexto visual.
**Escribe después el texto en pantalla.** De 2 a 6 palabras. Objetivo: intriga, no descripción. Tres categorías que funcionan:
- **Paradoja** — suena mal o contradictorio: "Ella tenía razón." / "Despedí a los tres." / "Me costó $20."
- **Brecha de prueba social** — implica que otros sabían algo antes: "78K personas sabían esto antes que yo."
- **Confesión** — crea tensión: "Casi no publico esto." / "Cotización de agencia: $5,000."

**Textos en pantalla que no funcionan:** etiquetas descriptivas, nombres de herramientas, frases sermoneadoras, cualquier cosa que repita o resuma el gancho hablado.

**Buen par (simultáneos — cada uno se sostiene solo, juntos crean contraste):**
- Hablado: "Publiqué durante 3 meses, no conseguí nada y lo dejé. Dos veces. Esto es lo que de verdad estaba haciendo mal."
- Texto: "Casi borro la cuenta." ← confesión que agrega tensión sin explicar el gancho hablado

---

## Paso 6: Resultado

Usa exactamente este formato:

---

**La Pregunta:**
[1-2 oraciones. Directa. La puerta que abre la historia del usuario.]

**La Semilla de la Historia:**
[2-3 oraciones. La experiencia real y específica de la vida del usuario de la que sale este video. Nombra el momento, la decisión, el error o el cambio — no la lección, el *hecho*.]

**Por qué ahora:**
[1 oración. Qué conversación viva hace que esto sea oportuno. Omítelo si no está ligado a una tendencia.]

**El "¿y qué?":**
[2 oraciones. Qué creencia cambia o qué decisión se desbloquea para el espectador. Basado en un resultado real para la audiencia — específico, no vago.]

---

**5 Ganchos:**

1. **[Sobre Mí]** — "[gancho]"
   *Texto en pantalla: "[2–6 palabras — paradoja / brecha de prueba social / confesión]"*

2. **[Si Yo]** — "[gancho]"
   *Texto en pantalla: "[2–6 palabras]"*

3. **[A Ti]** — "[gancho]"
   *Texto en pantalla: "[2–6 palabras]"*

4. **[¿Se Puede?]** — "[gancho]"
   *Texto en pantalla: "[2–6 palabras]"*

5. **[Él/Ella Acaba de]** — "[gancho]"
   *Texto en pantalla: "[2–6 palabras]"*

**Usa el gancho #[X].** [Una oración — por qué este gancho, citando el encaje con la audiencia.]

---

**El CTA:**
[Una oración. Solo seguir. Lo que acaban de recibir → lo que van a seguir recibiendo. Sin oferta, sin link.]

---

El usuario presiona grabar, no un menú. La semilla de la historia es el contenido. La pregunta es el punto de entrada. El gancho es la primera línea. El CTA es la última.
