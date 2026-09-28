---
name: daily-post-ideas
description: Genera 5 ideas personalizadas de posts de LinkedIn para el usuario, una por categoría de contenido, cada una con una línea de gancho lista para pegar y un ángulo de una línea. Úsalo siempre que el usuario pida ideas de posts de LinkedIn, diga "qué debería publicar hoy", "dame ideas de contenido para LinkedIn", "5 ideas de posts" o invoque /daily-post-ideas. Actívalo siempre para generar ideas de contenido de LinkedIn — incluso con pedidos casuales como "necesito publicar algo hoy" o "cuál es un buen tema de LinkedIn para mí".
---

# Ideas diarias de posts de LinkedIn

Genera 5 ideas de posts de LinkedIn — una por categoría — cada una con una línea de gancho que detenga el scroll y un ángulo breve. No hace falta búsqueda web ni información adicional. Todo sale del perfil de marca del usuario.

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia — yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## Proceso

1. Lee `~/.claude/brand-profile.md`. Toma la Audiencia, el Dolor principal, la Oferta, la Transformación, la Prueba, el Tono y las Palabras a evitar del usuario. Esto guía cada idea.

2. Si el usuario ejecutó el skill **positioning-filter**, aplica su ángulo fijado en silencio para que cada gancho suene a *él*, no a un consejo genérico. Si no lo hizo, trabaja solo con el perfil.

3. Toma nota de la fecha de hoy según el contexto por si hay alguna relevancia estacional u oportuna.

4. Genera exactamente 5 ideas, una por cada categoría de abajo. Usa el propio lenguaje de la audiencia en los ganchos — las palabras que realmente usarían, no lenguaje de marketing. No repitas el mismo formato ni el mismo ángulo dos veces.

## Formato de salida

Presenta las ideas exactamente en este formato:

---

**Aquí tienes 5 ideas de posts de LinkedIn para hoy:**

**1. Lección**
Gancho: [oración de apertura lista para pegar como primera línea de un post]
Ángulo: [una oración que describe hacia dónde va el post a partir de ahí]

**2. Opinión Polémica**
Gancho: [oración de apertura]
Ángulo: [una oración]

**3. Historia**
Gancho: [oración de apertura]
Ángulo: [una oración]

**4. Herramienta / Consejo Práctico**
Gancho: [oración de apertura]
Ángulo: [una oración]

**5. Atracción de Comunidad**
Gancho: [oración de apertura]
Ángulo: [una oración]

---

Después de las 5 ideas, agrega una línea:
> Elige una y di "escríbelo" para redactar el post completo.

## Definición de las categorías

**Lección** — Una idea específica que el usuario se ganó haciendo su trabajo real. Debe sentirse ganada, no genérica. Sácala de su Prueba o su Transformación cuando sea posible.

**Opinión Polémica** — Una opinión contraria o contraintuitiva sobre su industria o sobre cómo trabaja la gente en ella. Debe hacer que alguien deje de scrollear. No clickbait — una opinión real respaldada por experiencia.

**Historia** — Un momento detrás de escena: algo que salió mal y se arregló, un resultado sorprendente, un logro con un cliente, un cambio que importó. Lo específico le gana a lo vago.

**Herramienta / Consejo Práctico** — Una técnica concreta e inmediatamente aplicable del proceso del usuario. Energía de "este es el paso/ajuste/enfoque exacto". La audiencia debería poder usarla hoy.

**Atracción de Comunidad** — Un post que prioriza el valor y que hace que la oferta del usuario se sienta de forma natural como el siguiente paso obvio. Sin CTA directo, sin links. El propio contenido es el que atrae.

## Reglas de LinkedIn (se aplican siempre)

- Escribe todos los ganchos en **primera persona** — "yo", "mi", "me". Nunca uses el nombre del autor.
- **Sin links ni URLs externas** en ninguna parte de las ideas. Los links matan el alcance en LinkedIn.
- Mantén los ganchos en menos de 2 líneas — tienen que funcionar como la vista previa visible antes de "ver más".
- Los ganchos deben crear tensión, curiosidad o una opinión fuerte — no resumir el post.
- Respeta las Palabras a evitar del usuario según el perfil.

## Qué evitar

- Ganchos genéricos como "La IA lo está cambiando todo" o "Esto es lo que aprendí".
- Ideas que repiten el mismo formato o ángulo entre sí.
- Ganchos que necesitan contexto para funcionar — tienen que funcionar en frío.
- Mencionar la oferta del usuario en cada idea — solo en la Atracción de Comunidad.
