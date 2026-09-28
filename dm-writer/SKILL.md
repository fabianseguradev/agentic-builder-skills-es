---
name: dm-writer
description: Escribe un DM o mensaje corto y humano a una persona específica para un objetivo específico (iniciar una conversación, compartir tu oferta o hacer seguimiento) — con tu voz, para que abra un diálogo en lugar de soltarle un pitch en la cara. Actívalo siempre que el usuario diga "escribe un DM", "ayúdame a escribirle a esta persona", "qué le digo a", "contacta a [nombre]", "redacta un mensaje", "haz seguimiento con", "cómo le menciono mi oferta a" o "no sé cómo redactar esto".
---

# DM Writer — un mensaje real a una persona real

Un buen DM no es una difusión masiva. Es un mensaje a *esta* persona, que hace referencia a *esta* relación, con *una* razón clara para escribir. Este skill toma el contexto que le das y escribe un mensaje corto que suena a ti escribiéndole a alguien que respetas — no a un embudo.

Úsalo para una sola persona. Si quieres una lista completa y ordenada de a quién contactar primero, ejecuta **warm-outreach** primero y luego trae aquí a las personas una por una.

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia — yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## Pasos

### 1. Consigue las tres cosas que necesita un buen DM
Pídele al usuario esto (acepta respuestas cortas; deduce el resto del perfil):
- **Quién** — el destinatario: nombre, a qué se dedica y cualquier detalle que lo haga *él* (su trabajo, un post reciente, cómo se conocieron).
- **Relación** — qué tan bien lo conoces y cuándo hablaron por última vez (cercana, cálida-pero-en-silencio, apenas lo conoces, fría-pero-con-un-contacto-en-común).
- **Objetivo** — elige uno: **iniciar una conversación** (todavía sin pedido) · **compartir la oferta** (ha mostrado que encaja) · **hacer seguimiento** (ya le escribiste y quieres darle un empujoncito o reabrir).

Si el usuario solo da un nombre, haz las una o dos preguntas que de verdad cambian el mensaje — normalmente la relación y el objetivo.

### 2. Ajusta el mensaje a la relación
El registro cambia según la calidez, no según el objetivo:
- **Cercana / cálida:** casual, minúsculas sin problema, directo al punto, una pregunta real al final.
- **Cálida-pero-en-silencio:** primero reconecta. Reconoce el tiempo sin hablar con honestidad ("cuánto tiempo"), empieza con interés genuino por la persona, gánate el derecho a mencionar lo que estás construyendo.
- **Apenas lo conoces / contacto en común:** nombra al contacto en común o la razón específica por la que te vino a la mente desde el principio, mantenlo muy corto, haz que el pedido sea mínimo.

### 3. Escribe el mensaje — las reglas para no presionar
- **Empieza por ellos.** La primera línea trata del destinatario o del contexto compartido, nunca "Bueno, tengo esta oferta".
- **Una razón, un pedido.** Nada de links apilados, nada de pitch de varios párrafos, nada de historia de vida.
- **Termina con una pregunta fácil.** El objetivo es una respuesta, no un sí. Una pregunta que puedan responder en una línea le gana a un llamado a la acción.
- **Solo nombra la oferta si el objetivo es "compartir la oferta"** — e incluso entonces, plantéalo como "esto podría servirte porque [razón específica]", no como un volcado de funciones.
- Respeta las palabras a evitar y el tono del perfil. Nada de urgencia falsa, nada de gancho tipo "pregunta rápida", nada de halagos que el usuario no siente.
- Mantenlo en 2–5 oraciones. Si es más largo que un mensaje que de verdad mandarías, recórtalo.

### 4. Agrega un seguimiento de una línea
Incluye siempre **una sola** línea de seguimiento que el usuario pueda enviar si no hay respuesta después de unos días. Debe aportar valor o ligereza, nunca culpa ("solo reflotando esto" / "¿viste mi mensaje?"). Los buenos seguimientos mencionan algo nuevo, o dejan ir la conversación con elegancia ("no te preocupes si no es buen momento — la puerta queda abierta"). Un solo seguimiento, y luego detente.

### 5. Guárdalo
Agrega el mensaje + el seguimiento al final de `~/dm-drafts.md` bajo un encabezado con el nombre del destinatario y la fecha, para que el usuario vaya armando su propio archivo de referencia de lo que ha enviado. Confirma la ruta y recuérdale que cambie el detalle personal antes de enviarlo.

## Ejemplo de entrada → salida
**Entrada:** "Escríbele a Sam — hicimos un bootcamp juntos el año pasado, no hablamos hace meses. Tiene una pequeña agencia de Shopify. Objetivo: compartir mi oferta (construyo flujos automatizados de emails post-compra)."

**Salida (cálida-pero-en-silencio + compartir oferta):**
> ¡hola Sam! cuánto tiempo — ¿cómo le terminó yendo a la agencia después del bootcamp? de hecho me acordé de ti porque últimamente he estado construyendo flujos automatizados de emails post-compra para tiendas de Shopify, y recuerdo que tenías un montón de clientes que probablemente querrían eso. ¿vale la pena una charla rápida, o ahora mismo no es lo tuyo?

**Seguimiento (si no hay respuesta en ~4 días):**
> sin presión de ninguna forma, Sam — si los flujos post-compra no son prioridad ahora mismo, todo bien. igual me encantaría ponernos al día en algún momento.

Guardado en `~/dm-drafts.md`.

## Notas / casos especiales
- Si el objetivo es "compartir la oferta" pero la relación es fría y no hay ninguna señal real de que encaje, dilo — recomienda la versión de "iniciar una conversación" en su lugar. Hacerle un pitch a un desconocido es exactamente el movimiento que hace que vender se sienta desagradable y no funciona.
- Nunca inventes un recuerdo compartido ni un resultado. Si el espacio del detalle personal no se puede llenar con la verdad, el mensaje baja a un registro más ligero.
- Un mensaje, un seguimiento. Si quieren una secuencia completa o una lista de personas, eso es el skill **warm-outreach** — no más seguimientos a una sola persona.
