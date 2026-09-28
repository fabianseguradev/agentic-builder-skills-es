---
name: email-writer
description: Escribe el email que has estado postergando — cobrar una factura impaga, decir que no, disculparte por un error, pedir un aumento o una subida de tarifa, el tercer seguimiento o dar una mala noticia. Hace tres preguntas rápidas (quién es esa persona para ti, qué quieres que pase, qué tan directo puedes ser) y te devuelve un email corto con un pedido claro cerca del principio, con tu voz. Úsalo cuando el usuario diga "escribe un email", "ayúdame a escribir este email", "necesito escribirle un email a alguien", "cómo digo que no a esto", "cobrar una factura", "no me han pagado", "email de seguimiento", "necesito disculparme", "pedir un aumento", "el email que he estado evitando", "no sé cómo redactar esto" o /email-writer.
---

# Email Writer — el que has estado evitando

La mayoría de los emails difíciles no se envían porque la persona no encuentra el tono. Entonces escriben cuatro párrafos de rodeos y entierran el pedido real en la última línea, donde nadie lo lee. Este skill hace lo contrario: un pedido, cerca del principio, en palabras simples que suenan a ti. Recibes un asunto y un cuerpo que puedes pegar y enviar.

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia — yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## Pasos

### 1. Nombra el tipo de email
Lee lo que te dio el usuario y clasifícalo en uno de estos seis. Si no es ninguno, trátalo como un pedido general y sigue adelante.

- **Cobrar dinero** — una factura está atrasada.
- **Decir que no** — rechazar un trabajo, un favor, una llamada, un descuento.
- **Disculparse** — se te pasó algo, rompiste algo, llegaste tarde.
- **Pedir más** — un aumento, una subida de tarifa, mejores condiciones.
- **Tercer seguimiento** — ya insististe dos veces y no has sabido nada.
- **Mala noticia** — un retraso, una subida de precio, una cancelación, un despido.

Di cuál elegiste en una línea. Cada tipo tiene una regla que debes seguir, listada en el paso 4.

### 2. Haz las tres preguntas
Hazlas juntas, en un mensaje corto. Nunca hagas más de tres.

1. **¿Quién es esta persona para ti?** (un cliente que te paga, tu jefe, alguien a quien vas a necesitar de nuevo, alguien con quien nunca más vas a tratar)
2. **¿Qué quieres que pase de verdad después de que lo lea?** Un resultado. "Que pague la factura antes del viernes." "Que acepte £X." "Que deje de pedirlo."
3. **¿Qué tan directo puedes ser?** Cálido / directo / firme. Si no lo saben, usa directo.

Si el usuario ya te dijo esto en su primer mensaje, no vuelvas a preguntar — di lo que dedujiste y continúa.

### 3. Consigue los datos que no puedes inventar
Pide solo lo que de verdad necesitas para escribirlo: montos, fechas, número de factura, qué se prometió, qué salió mal. Si falta un dato, escribe `[COMPLETAR]` en el borrador en lugar de inventar algo. Nunca inventes un número, una fecha ni una promesa.

### 4. Escribe el email — un pedido, cerca del principio
Estructura cada email así:

- **Asunto:** simple y específico. "Factura 104 — ya 3 semanas vencida" le gana a "Pregunta rápida".
- **Línea 1:** una oración de contexto para que sepan por qué escribes.
- **Línea 2 o 3:** el pedido. Qué quieres y para cuándo. Esta es la regla — el pedido nunca vive al final.
- **Medio:** la razón breve, solo si les ayuda a decir que sí.
- **Cierre:** una línea, sin arrastrarse.

Mantenlo en menos de 150 palabras. Párrafos cortos, de una a tres líneas cada uno. Nada de "Espero que este email te encuentre bien". Nada de "solo retomando esto". Nada de disculparte por existir.

Reglas por tipo, aplica la que corresponda:
- **Cobrar dinero:** indica el monto, el número de factura y la fecha de vencimiento original. Pide una fecha de pago, no "una actualización". Mantente neutral — asume que es un descuido hasta que se demuestre lo contrario. Agrega el siguiente paso si lo ignoran solo en el tercer cobro.
- **Decir que no:** di que no en las dos primeras líneas. No dejes abierta una puerta que no quieres dejar abierta. Una oración de razón, no un ensayo. Ofrece una alternativa solo si de verdad la quieres ofrecer.
- **Disculparse:** asúmelo con claridad, nada de "si te sentiste". Di qué estás haciendo al respecto. Una disculpa, no cuatro. No expliques más de lo que cabe en una oración.
- **Pedir más:** empieza con lo que quieres y el número. Luego dos líneas de evidencia — resultados, alcance adicional, tarifa de mercado. Nunca te disculpes por pedir. Nunca abras con "Sé que corren tiempos difíciles".
- **Tercer seguimiento:** menciona el hecho de que es el tercero. Haz que sea fácil cerrar el tema: "Si esto ya no va a suceder, solo responde 'no' y cierro el expediente." Esa línea consigue más respuestas que cualquier insistencia.
- **Mala noticia:** la noticia va en la primera oración, antes de la razón. Luego qué estás haciendo al respecto, luego qué necesitas de ellos. Nunca la entierres en el tercer párrafo.

### 5. Ajústalo a su voz
Reescríbelo una vez usando el tono, las palabras favoritas y las palabras prohibidas del perfil de marca. Léelo como si fueras el destinatario y pregúntate: ¿el pedido es obvio en los primeros cinco segundos? Si no, súbelo.

### 6. Dales una versión más suave y una más dura de una línea
Elige la línea que carga más riesgo — normalmente el pedido. Ofrece dos alternativas: una más cálida y una más firme. Una línea cada una. Que puedan cambiarla sin reescribir nada más.

## Resultado — guárdalo
Escribe el email en `~/emails/<short-slug>-<YYYY-MM-DD>.md` (crea `~/emails/` si no existe). Incluye: el asunto, el cuerpo completo y las líneas alternativas más suave/más firme al final bajo un encabezado `## Alternativas`.

Dile al usuario la ruta y di: pégalo, reemplaza cualquier `[COMPLETAR]`, envíalo hoy. Nada de un email difícil se vuelve más fácil por dejarlo para mañana.

## Ejemplo (entrada → salida)
**Entrada:** "Un cliente me debe £1,800 de una factura que mandé hace cinco semanas. Ya le insistí una vez. Quiero volver a trabajar con él, así que no quiero ser agresivo."

**Salida (guardada en `~/emails/invoice-104-chase-2026-07-30.md`):**

> **Asunto:** Factura 104 — £1,800, ya 5 semanas vencida
>
> Hola Sam:
>
> La factura 104 por £1,800 vencía el 25 de junio y en mis registros todavía figura como impaga.
>
> ¿Puedes confirmarme una fecha de pago esta semana? Si está trabada en su sistema de finanzas, dime a quién enviársela y la sigo por ahí.
>
> Con gusto seguimos avanzando con el próximo proyecto en cuanto cerremos este.
>
> Gracias,
> Alex
>
> **## Alternativas**
> - Pedido más cálido: "Sin apuro hoy — solo avísame más o menos cuándo es probable que llegue."
> - Pedido más firme: "Necesito una fecha de pago antes del viernes para programar cualquier trabajo adicional."

## Notas / casos especiales
- El error de principiante que esto evita: escribir 300 palabras de disculpas y enterrar el pedido en la última línea. Si el borrador no plantea el pedido antes de la línea tres, reescríbelo.
- Si la entrada es escasa ("necesito escribirle a mi jefe"), haz las tres preguntas y detente. No adivines cómo es la relación.
- Si el email involucra un contrato, un despido, dinero adeudado durante mucho tiempo o cualquier cosa que pueda terminar en un proceso legal, escríbelo de forma simple y agrega una línea: "Vale la pena que un profesional revise este antes de enviarlo." No des asesoría legal.
- Si el usuario está enojado, escribe la versión que se puede enviar, no la honesta. Ofrece guardar la versión enojada en un archivo aparte que no se envía.
- Si el mensaje que recibieron es largo y confuso, ejecuta primero **doc-digest** sobre él y luego vuelve aquí para responder.
- Si después de todo esto el borrador suena rígido o corporativo, ejecuta **rewrite-plain** sobre él.
