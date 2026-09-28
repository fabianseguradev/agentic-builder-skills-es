---
name: first-customer-closer
description: Convierte "alguien está interesado pero no sé cómo vender de verdad" en un guion de conversación tranquilo y honesto usando el marco CLOSER — hecho para gente que odia vender. Produce un guion personalizado para llamada o DM, las preguntas exactas que hay que hacer, cómo invitar a la venta sin presionar y cómo manejar el "déjame pensarlo". Actívalo siempre que el usuario diga "alguien está interesado y no sé qué decir", "tengo una llamada de ventas", "cómo cierro", "ayúdame a vender sin sonar vendedor", "escríbeme un guion de ventas", "alguien respondió que sí", "entré a una llamada y me congelé" o "cómo pido la venta de verdad".
---

# First-Customer Closer — una conversación de ventas para gente que odia vender

Alguien levantó la mano. Ahora estás en pánico, porque "cerrar" suena a una jugada de vendedor de autos usados que nunca quieres hacer. Este es el cambio de enfoque: una buena conversación de ventas es simplemente **ayudar a alguien a tener claro si esto es lo correcto para él.** Haces preguntas honestas, escuchas y, si encaja, haces que sea fácil decir que sí. Si no encaja, lo dices — eso es lo que te hace confiable.

Este skill te arma un guion de una página alrededor del marco **CLOSER** para que entres sabiendo exactamente qué preguntar y qué decir.

**CLOSER** = **C**larify (aclara por qué están aquí) · **L**abel (nombra el problema) · **O**verview (repasa lo que ya intentaron) · **S**ell (vende el resultado — las vacaciones, no el avión) · **E**xplain (disipa las preocupaciones) · **R**einforce (refuerza la decisión).

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia — yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## Pasos

### 1. Entiende la situación
Pídele al usuario:
- **Quién** es el prospecto y a qué se dedica.
- **Cómo llegó** (respondió a un DM, agendó una llamada, preguntó por la oferta en un evento).
- **El formato** — ¿llamada en vivo, o ida y vuelta por DM/notas de voz? (El guion se adapta: una llamada es hablada y fluida; por DM son turnos más cortos, una pregunta a la vez.)
- **La oferta + el precio** (tómalos del perfil si están definidos).

### 2. Arma el guion CLOSER
Escribe un guion hablado y humano — no un formulario para leer como robot — a través de las seis etapas. Para cada etapa, dale al usuario **el objetivo en una línea + las palabras exactas que decir**, con su voz:

- **C — Clarify: aclara por qué están aquí.** Abre haciendo que *ellos* hablen de por qué te escribieron. *"Antes de contarte nada sobre lo que hago — ¿qué te hizo escribirme? ¿Qué está pasando ahora mismo?"* Así la conversación es de ellos, no tu pitch.
- **L — Label: nombra el problema.** Devuélveles el problema real con sus palabras para que se sientan entendidos. *"Entonces parece que lo central es [X] — ¿esa es la parte que de verdad te está costando?"* No avances hasta que lo confirmen.
- **O — Overview: repasa lo que ya intentaron.** *"¿Qué has intentado ya para resolver esto?"* Esto saca a la luz por qué fallaron los intentos anteriores (normalmente es justo el hueco que llena la oferta) y evita que vuelvan a probar la versión gratis después de la llamada.
- **S — Sell: vende el resultado, no las funciones.** Describe el *después* — su vida una vez que el problema desaparece — no la mecánica de cómo funciona. *"Ya no tendrías que pensar en [X] — simplemente funcionaría solo."* La gente compra las vacaciones, no el vuelo. Nombra la oferta y el precio claramente aquí, una vez, sin titubear.
- **E — Explain: disipa las preocupaciones.** Invita las objeciones en lugar de esquivarlas. *"¿Qué te está haciendo dudar?"* Luego manéjalo con honestidad (combínalo con el skill **objection-handler** para tener un banco completo de respuestas).
- **R — Reinforce: refuerza la decisión.** Después de un sí, recuérdales que tomaron una decisión inteligente y fija el siguiente paso concreto. *"Te vas a alegrar de haber hecho esto — esto es exactamente lo que pasa ahora."*

### 3. Escribe la lista de preguntas clave
Saca las 5–7 preguntas que el usuario tiene que hacer (sobre todo de C, L, O). Un vendedor nervioso que tiene las preguntas en una nota adhesiva siempre le gana a uno que improvisa. Estas preguntas hacen la venta — el prospecto se convence solo.

### 4. Escribe el momento de "invitar a la venta"
La mayoría de la gente que no es vendedora se congela justo aquí, así que escríbelo de forma explícita. Una invitación limpia y tranquila — sin presión, sin cuenta regresiva:
> *"Por todo lo que me dijiste, de verdad creo que esto te ayudaría. ¿Quieres que empecemos?"*
Luego **deja de hablar.** El silencio no es tu enemigo. Da una versión para llamada y una versión para DM.

### 5. Maneja el "déjame pensarlo"
Esto casi siempre significa una preocupación no dicha, no una necesidad real de tiempo. Escribe una respuesta cálida que la saque a la luz sin presionar:
> *"Totalmente válido. Solo para poder ayudarte — ¿es el precio, el momento, o no estás seguro de que funcione para tu situación?"*
Sea lo que sea que nombren, abórdalo con honestidad y luego vuelve a ofrecer *una vez*. Si sigue siendo no, deja la puerta abierta con elegancia — una buena salida los mantiene como un futuro sí.

### 6. Guarda el guion
Escribe el guion completo de una página en `~/first-customer-script.md`: las seis etapas de CLOSER con las palabras que decir, la lista de preguntas, la línea de invitación y la rama del "déjame pensarlo". Confirma la ruta y dile al usuario que lo lea en voz alta una vez antes de la conversación para que suene a él, no a un guion.

## Ejemplo de entrada → salida
**Entrada:** "Alguien de mi newsletter agendó una llamada. Tiene un estudio de yoga. Mi oferta es una configuración de automatización de reservas de $600." (llamada de voz)

**Salida — `~/first-customer-script.md` (extracto):**

**C — Clarify:** *"Antes de entrar en tema — ¿qué te hizo agendar esta llamada? ¿Qué está pasando con el estudio ahora mismo?"*
**L — Label:** *"Entonces el costo real son las ausencias y las horas que pasas persiguiendo reservas — esa es la parte que te está desangrando, ¿no?"*
**S — Sell (el resultado):** *"Imagina el lunes: reservas, recordatorios, lista de espera — todo resuelto sin que toques el teléfono. Eso es lo que hace esto. Es una configuración única de $600."*
**Invitación:** *"De verdad creo que esto te quitaría eso de encima. ¿Empezamos?"* → (deja de hablar)
**"Déjame pensarlo":** *"Claro. Una cosa rápida para poder ayudarte de verdad — ¿son los $600, el momento, o no estás segura de que se adapte a cómo funciona tu estudio?"*

**Preguntas para hacer:** por qué ahora · cuánto te está costando · qué has intentado · qué cambiaría si se resolviera · cuál es tu duda.

## Notas / casos especiales
- Si de verdad no encaja, lo honesto es decirlo y quizás recomendarles otra opción. No es solo ética — es lo que hace que los síes sean reales y que lleguen las recomendaciones.
- No acumules invitaciones. Pregunta una vez, quédate en silencio, deja que respondan. Volver a preguntar de inmediato se lee como desesperación y rompe la confianza.
- Di el precio de forma llana y segura. Si el usuario tiende a sobreexplicar o a hacer descuentos en el momento, márcalo en el guion con una nota de "di el precio y luego detente".
- Para las respuestas a objeciones de la etapa E, pasa a **objection-handler** para armar una hoja de referencia completa que el usuario tenga junto a este guion.
