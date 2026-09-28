---
name: proposal-writer
description: Convierte las notas desordenadas de una llamada con un posible cliente en un documento de propuesta limpio y listo para enviar. Es lo que mandas por escrito después de haber fijado tu precio y haber tenido la conversación. Reformula su problema con sus propias palabras, muestra el resultado, enumera exactamente lo que obtienen y luego pone el precio donde ya se siente justificado. Se guarda como un archivo markdown que puedes copiar directamente en un email. Úsalo cuando el usuario diga "escribe una propuesta", "tuve una llamada, ¿ahora qué les mando?", "convierte estas notas en una propuesta", "mándales una cotización", "me pidieron que lo pusiera por escrito", "cómo redacto esto" o escriba /proposal-writer.
---

# Proposal Writer: el documento que envías después de la llamada

Alguien habló contigo. Está interesado. Ahora lo quiere por escrito, y tú estás mirando una página en blanco.

Una propuesta no es una lista de precios con tu logo. Es un documento corto que le muestra al comprador que entendiste su problema, pinta lo que cambia cuando se resuelve y luego nombra el precio cuando ya quiere la cosa. Si aciertas con ese orden, el número deja de dar miedo. Este skill escribe ese documento a partir de las notas que tengas, y lo guarda como un archivo que puedes pegar en un email.

## Personalización
Este skill trabaja con *tu* voz. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize**, o simplemente dime tu nombre, a qué te dedicas y para quién lo haces, y yo lo creo.
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario. Usa solo lo que está en el perfil, o pregunta.

## Lo que necesito de ti
Pega lo que tengas. Notas rápidas de la llamada, una nota de voz que transcribiste, unas cuantas viñetas, todo sirve. Te preguntaré lo que falte.

1. **¿Para quién es?** Su nombre, su negocio, a qué se dedica.
2. **¿Qué dijeron que necesitan?** Sus palabras exactas si las anotaste. Su propia forma de decirlo es lo más valioso de tus notas.
3. **¿Qué quieren que sea cierto después?** Cómo se ve para ellos que "esto funcionó".
4. **¿Qué vas a hacer por ellos?** El trabajo real. Esto es el alcance, es decir, la lista de lo que entra en el trabajo y lo que no.
5. **Tu precio.** Un número está bien.
6. **Plazos.** Cuándo puedes empezar y más o menos cuánto toma.
7. **Cualquier garantía con la que te sientas cómodo.** Opcional. Sáltatela si nada se siente seguro de prometer.

## Pasos

### 1. Lee las notas y encuentra los huecos
Toma del perfil su voz y cualquier prueba real que ya tengan. Luego lee las notas y comprueba las tres piezas que sostienen todo: el problema del comprador, el alcance y el precio.

Si falta alguna de esas tres, pregunta antes de escribir. No voy a adivinar un precio ni a inventar un alcance. Todo lo demás lo puedo resolver.

### 2. Reformula el problema con su lenguaje
Esta es la sección que lo decide todo. Si el comprador no se siente entendido aquí, ningún precio le va a parecer razonable.

Dos o tres oraciones que describan dónde están ahora, usando las palabras que usaron en la llamada. Concreto y específico de su negocio, no una versión genérica de los problemas de su industria.

Si el usuario no anotó las palabras exactas del comprador, escríbelo de forma simple a partir de las notas. Nunca fabriques una cita y la pongas en boca de alguien.

### 3. Escribe el resultado
Qué es diferente en su negocio una vez que esto está hecho. Concreto. Conéctalo con algo de la sección del problema para que las dos mitades encajen.

No "mejora de la eficiencia". Algo como "tu recepción deja de reservar dos veces el mismo horario y las diez personas al mes que se van porque reservar es un fastidio se quedan con su reserva".

### 4. Enumera los entregables
Una lista limpia de viñetas con exactamente lo que obtienen. Contable y específica.

Bien: "3 diseños de landing page, más 2 rondas de cambios."
Mal: "trabajo de diseño."

Las listas específicas hacen dos trabajos a la vez. Hacen que el precio se sienta como algo que compra algo real, y protegen al usuario más adelante cuando el comprador pide una cuarta cosa que nunca estuvo en la lista.

### 5. Arma la sección de precio
Pon el precio después del resultado, nunca antes. Ese orden se llama anclaje: lo que el lector ve primero define cómo se siente todo lo que viene después. Muestra primero el valor y el número cae contra el valor en lugar de contra nada.

Por defecto, **dos opciones** en una tabla pequeña:

| Opción | Qué incluye | Precio |
|---|---|---|
| Básico | el entregable central por sí solo | precio más bajo |
| **Completo (recomendado)** | lo central más las partes que de verdad consiguen el resultado | su precio |

Pon el número del usuario como **Completo** y márcalo como recomendado. Arma el Básico quitando las piezas que no son estrictamente necesarias, y ponle un precio honesto para ese trabajo más pequeño.

Dos opciones le ganan a una, porque un comprador que elige entre dos cosas está decidiendo *cuál*, no *si*. Dos también le ganan a tres en una primera venta, porque un tercer nivel premium suele significar prometer un trabajo continuo que el usuario nunca ha entregado antes.

Si ya ejecutaron **pricing-calculator** y tienen tres niveles que de verdad pueden entregar, usa los tres.

Nunca cambies un número que te dio el usuario. Sugiere la estructura, deja que ellos fijen el precio.

### 6. Agrega la garantía, solo si tienen una
Una garantía, a veces llamada inversión del riesgo, es que tú asumas parte del riesgo para que el comprador no cargue con todo. "Si no está en línea para la fecha de entrega, no pagas la mitad final."

Si el usuario no tiene una con la que se sienta cómodo, quita la sección. Una garantía que no pueden cumplir es peor que ninguna garantía.

### 7. Termina con un siguiente paso
Una acción, escrita como una oración que el comprador puede hacer en diez segundos. "Responde 'sí' y te mando la factura y un formulario corto de inicio. Empezamos el lunes."

Nunca termines con "avísame qué te parece". Así es como una propuesta queda sin leer durante tres semanas.

### 8. Revisa la voz
Aplica el tono del perfil. Simple y seguro, como le hablarían a alguien que respetan. Nada de "nos complace presentarle". Nada de rodeos. Todo el documento debería poder leerse en menos de dos minutos.

## Resultado: guárdalo
Escribe la propuesta en `~/proposals/proposal-<client-slug>-<YYYY-MM-DD>.md`, creando la carpeta `~/proposals/` si no está.

El archivo contiene, en este orden: título y fecha, el problema, el resultado, lo que obtienen, los plazos, la tabla de precios, la garantía si la hay y el siguiente paso.

Dile al usuario la ruta. Luego ofrécele una cosa: un email o DM corto para enviarla, de tres o cuatro líneas, para que la propuesta no llegue sola.

## Ejemplo (entrada → salida)
**Entrada:** "Hablé con María, tiene un estudio de Pilates, 3 sedes. Las reservas son en papel y por mensaje. Reserva dos veces el mismo horario todo el tiempo, calcula que pierde unos 10 clientes al mes porque reservar es un fastidio. Quiere reservas en línea que su recepción pueda manejar sin capacitación. Yo haría el sitio de reservas y los recordatorios automáticos. Estoy pensando en $3,500. Puedo empezar la semana que viene, unas 3 semanas de trabajo."

**Salida (extracto, guardado en `~/proposals/proposal-maria-pilates-2026-08-08.md`):**

> **Propuesta para María, [Nombre del estudio]. 8 de agosto de 2026**
>
> **Dónde estás ahora**
> Tres sedes, todas con reservas en papel y por mensaje de texto. Estás reservando dos veces el mismo horario, tu recepción está desbordada y unos diez clientes al mes se van porque reservar cuesta más esfuerzo de lo que vale. Son personas que ya te eligieron y que perdiste en la puerta.
>
> **Adónde te lleva esto**
> Una sola página de reservas para los tres estudios que tu recepción puede manejar desde el primer día, recordatorios automáticos para que la gente se presente y se acabaron las reservas duplicadas. Los diez clientes al mes mantienen su reserva.
>
> **Lo que obtienes**
> - Sitio de reservas en línea con tu marca para las 3 sedes
> - Recordatorios automáticos por mensaje de texto y email
> - Una vista simple para la recepción, sin necesidad de capacitación
> - 2 rondas de cambios y una llamada de recorrido de 30 minutos
>
> **Plazos:** empezamos el lunes, en línea en 3 semanas.
>
> **Precio**
>
> | Opción | Qué incluye | Precio |
> |---|---|---|
> | Básico | Solo el sitio de reservas | $2,200 |
> | **Completo (recomendado)** | Sitio de reservas, recordatorios, vista de recepción, recorrido | **$3,500** |
>
> **Mi garantía:** si las reservas no están en línea y funcionando en las tres sedes para la fecha de entrega, no pagas la segunda mitad.
>
> **Siguiente paso:** responde "vamos" y te mando la factura y un formulario corto de inicio. Empezamos el lunes.

## Notas / casos especiales
- El precio siempre lo decide el usuario. Sugiere la estructura, nunca muevas el número.
- Si las notas son escasas, haz tres preguntas y detente. No escribas una propuesta construida sobre suposiciones, porque el comprador lo va a notar en la sección del problema.
- Si todavía no eligieron un número, mándalos primero a **pricing-calculator** y luego vuelve aquí.
- Si el comprador en realidad no aceptó recibir una propuesta, todavía no la necesita. Eso es una conversación, y de eso se encarga **first-customer-closer**.
- Largo no significa serio. Una propuesta de una página que da en el clavo con el problema le gana siempre a seis páginas de diagramas de proceso.
- Envíala el mismo día si puedes. El interés se apaga rápido, y una propuesta que llega cuatro días después tiene que reconstruir toda la conversación.
