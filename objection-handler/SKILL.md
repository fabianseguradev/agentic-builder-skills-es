---
name: objection-handler
description: Convierte las objeciones que de verdad escuchas ("es demasiado caro", "no tengo tiempo", "déjame pensarlo", "¿esto funciona para alguien como yo?") en respuestas tranquilas y honestas que puedes dar sin congelarte ni presionar — adaptadas a TU oferta. Produce una hoja de referencia de objeciones y respuestas guardada, usando reconocer → reencuadrar → evidencia → invitar. Actívalo siempre que el usuario diga "cómo respondo cuando dicen", "manejar objeciones", "me dijeron que es demasiado caro", "qué le digo a un no tengo tiempo", "la gente me sigue diciendo", "nunca sé qué responder" o "ayúdame a responder a las objeciones".
---

# Objection Handler — respuestas honestas a lo que la gente de verdad dice

Una objeción no es un rechazo. Normalmente es una preocupación real y razonable que la persona necesita que le respondan antes de poder decir que sí. El problema es que la gente que no es vendedora o cede al instante ("¡ah, no te preocupes!") o se pone a la defensiva — ambas pierden la venta *y* se sienten mal. Este skill te arma una hoja de referencia para que, cuando escuches la objeción, ya tengas lista una respuesta tranquila, honesta y sin presión, con tu voz.

El patrón de cada respuesta: **reconocer** (hacer que se sientan escuchados) → **reencuadrar** (ayudarlos a verlo de otra forma) → **evidencia** (una razón verdadera por la que se sostiene) → **invitar** (un siguiente paso ligero, nunca un empujón).

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia — yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## Pasos

### 1. Reúne las objeciones reales
Empieza por las cuatro que escucha casi todo el mundo y luego pregúntale al usuario cuáles recibe *de verdad* y qué más aparece:
- **"Es demasiado caro."**
- **"Ahora mismo no tengo tiempo."**
- **"Déjame pensarlo."**
- **"¿Esto de verdad funciona para alguien como yo / mi situación?"**

Pregunta: "¿Cuáles de estas escuchas más, y hay una en particular que siempre te descoloca?" Agrega cualquier objeción específica de la oferta que nombren (p. ej., "podría construir esto yo mismo", "ya me quemé antes"). Maneja las objeciones que realmente enfrentan — una lista genérica que nunca van a usar no vale nada.

### 2. Entiende la oferta lo suficiente como para responder con honestidad
Toma del perfil la oferta, el precio, la transformación y cualquier prueba real. El paso de **evidencia** tiene que ser *verdadero* — un resultado real, una garantía genuina, un reencuadre honesto del valor. Si todavía no hay pruebas, la evidencia se apoya en la lógica honesta de la oferta y en algo que reduzca el riesgo (un primer paso pequeño, una garantía), nunca en un testimonio inventado.

### 3. Escribe el banco de respuestas
Para cada objeción, escribe una respuesta que siga reconocer → reencuadrar → evidencia → invitar, con la voz del usuario:
- **Reconocer** — de verdad, no como táctica. "Totalmente válido" / "Te entiendo."
- **Reencuadrar** — cambia el marco con honestidad. Precio → el costo de *no* resolverlo, o el precio por resultado. Tiempo → esto te *devuelve* tiempo. "Déjame pensarlo" → cuál es la duda real que hay debajo. "¿Funciona para mí?" → la razón específica por la que encaja con su situación.
- **Evidencia** — una razón verdadera y concreta: un resultado, una garantía, una comparación o una lógica clara. Nunca inventada.
- **Invitar** — un siguiente paso de baja presión: una pregunta, un primer paso pequeño o simplemente dejar la puerta abierta. Nunca una cuenta regresiva ni un chantaje emocional.

Dale a cada objeción **una respuesta principal** más una **versión corta de una línea** para DMs, donde un párrafo sería demasiado.

### 4. Agrega la regla de oro y la salida elegante
Dos cosas al principio de la hoja:
- **Pregunta antes de responder.** La mejor respuesta a casi cualquier objeción es primero una pregunta: *"Cuando dices que es demasiado caro — ¿es más de lo que esperabas, o es el momento?"* No puedes manejar la objeción real hasta saber cuál es. La mitad de los "es demasiado caro" en realidad son "no estoy seguro de que funcione".
- **El no honesto.** Escribe una salida cálida para cuando de verdad no encaja o no es el momento — porque estar dispuesto a escuchar un no es exactamente lo que hace que los síes sean confiables y mantiene la puerta abierta para más adelante.

### 5. Guarda la hoja de referencia
Escribe todo en `~/objection-cheatsheet.md`: la regla de oro arriba, luego cada objeción con su respuesta completa + la versión corta para DM, y la salida elegante al final. Confirma la ruta y dile al usuario que la repase antes de cualquier conversación de ventas para que las respuestas se sientan listas, no ensayadas.

## Ejemplo de entrada → salida
**Entrada:** Oferta (del perfil): "Configuración de automatización de reservas de $600 para estudios pequeños." El usuario escucha sobre todo "es demasiado caro" y "déjame pensarlo".

**Salida — `~/objection-cheatsheet.md` (extracto):**

**Regla de oro:** pregunta antes de responder. "Cuando dices que es mucho — ¿es más de lo que tenías presupuestado, o no estás seguro de que vaya a rendir?"

**"Es demasiado caro."**
> Totalmente válido — $600 es dinero de verdad. Pero mira cómo lo vería yo: ahora mismo las ausencias y las horas que pasas persiguiendo reservas te están costando mucho más que eso cada mes. Esta es una configuración única que tapa la fuga. Si te ahorra aunque sea unas pocas reservas, ya se pagó sola. ¿Quieres que te muestre exactamente qué resolvería para tu estudio?

*Corta (DM):* válido — pero las ausencias ya te están costando más de $600 al mes. esto tapa esa fuga una sola vez. ¿quieres el desglose rápido?

**"Déjame pensarlo."**
> Claro. ¿Puedo preguntarte — es el precio, el momento, o no estás del todo segura de que funcione para cómo trabaja tu estudio? Sea lo que sea, prefiero responderlo ahora que dejarte con la duda.

**Salida elegante:**
> Honestamente, si no es el momento, cero presión — prefiero que lo hagas cuando de verdad te ayude. Aquí estoy cuando estés lista.

## Notas / casos especiales
- El paso de evidencia es la línea de integridad: nunca inventes un resultado, una cantidad de clientes ni una garantía que el usuario no pueda cumplir. Si las pruebas son escasas, usa lógica honesta + algo que reduzca el riesgo.
- Si una objeción en realidad es un "no", respétala. Pasar por encima de un no genuino es lo que hace que vender se sienta desagradable y quema la relación para cualquier sí futuro.
- Se combina directamente con **first-customer-closer** (esta es la etapa "E — Explain: disipa las preocupaciones" de ese guion) y con **dm-writer** para las versiones cortas de DM.
