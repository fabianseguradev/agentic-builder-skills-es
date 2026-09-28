---
name: offer-builder
description: Construye una "Grand Slam Offer" al estilo Hormozi, tan buena que la gente se sienta tonta diciendo que no — diseñada alrededor de la Ecuación de Valor (un resultado soñado más grande, más confianza en que va a funcionar, menos tiempo, menos esfuerzo). Úsalo cuando el usuario diga "construye mi oferta", "haz que mi oferta sea irresistible", "ayúdame a empaquetar lo que vendo", "no sé cómo ponerle precio/presentar esto", "grand slam offer", "construí un producto pero nadie compra", o cuando tenga algo para vender pero ninguna forma convincente de presentarlo. Insiste en ejecutarlo antes de que intenten vender cualquier cosa.
---

# Offer Builder — diseña una Grand Slam Offer

Convierte "este es mi producto" en una oferta tan cargada y sin riesgo que el prospecto se sienta tonto dejándola pasar. Guías al usuario por la Ecuación de Valor, apilas entregables que eliminan cada uno un obstáculo específico, y luego le pones nombre y le agregas una garantía, urgencia y bonos. El resultado es una oferta escrita y lista para presentar, más una frase grand slam de una línea que pueden decir en voz alta.

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia — yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## La idea en un respiro
La gente compra cuando el valor percibido es alto. El valor SUBE cuando el **resultado soñado** es más grande y la **probabilidad de que de verdad lo logren** se siente más alta. El valor BAJA cuanto más **tiempo** toma y cuanto más **esfuerzo y sacrificio** cuesta. Así que una gran oferta maximiza los dos de arriba y aplasta los dos de abajo. Todo lo que sigue es simplemente hacer eso a propósito.

## Pasos

### 1. Ancla el resultado soñado
Pregúntale al usuario (o sácalo de la Audiencia + Transformación del perfil): *¿qué es lo que más quiere tu comprador del otro lado de esto?* Hazlo concreto y emocional — no "aprender marketing" sino "conseguir tu primer cliente que paga en 30 días sin llamadas en frío". Escríbelo como la promesa principal. Esta es la parte de arriba de la Ecuación de Valor.

### 2. Enumera los obstáculos (esta es la mina de oro)
Pregunta: *¿qué le impide a tu comprador conseguir ese resultado por su cuenta?* Consigue de 4 a 8 obstáculos reales — los miedos, las habilidades que faltan, el tiempo que consume, los fracasos pasados, el "no sé por dónde empezar". Cada obstáculo es un bache que la oferta va a allanar. Escríbelos como una lista.

### 3. Apila entregables — uno por obstáculo
Para cada obstáculo, inventa un entregable que lo elimine. Este es el movimiento central: la oferta no es una cosa, es una pila donde cada elemento elimina visiblemente una objeción.
- Obstáculo "no sé por dónde empezar" -> una hoja de ruta o checklist paso a paso.
- Obstáculo "no tengo tiempo" -> plantillas hechas por ti / un sprint hecho en conjunto.
- Obstáculo "¿y si no funciona para mí?" -> una revisión en vivo o una llamada 1:1.
- Obstáculo "ya fracasé antes" -> un marco probado + ejemplos.
Escribe cada entregable junto al obstáculo que resuelve, y dale a cada uno un nombre tangible y un valor aproximado por sí solo.

### 4. Ataca la parte de abajo de la ecuación
Ahora recorta el tiempo y el esfuerzo de forma explícita:
- **Tiempo de espera:** ¿cuál es la primera victoria más rápida, y puedes nombrar un plazo? ("primer resultado en 7 días"). Pon una victoria rápida al principio.
- **Esfuerzo y sacrificio:** ¿qué puedes hacer por ellos, convertir en plantilla o automatizar para que hagan menos? Cada "lo hacemos por ti" sube el valor.

### 5. Ponle nombre a la oferta
Dale a toda la pila un nombre que implique el resultado (no el mecanismo). "El Sistema de Primer Cliente en 30 Días" le gana a "Mi Paquete de Coaching". Mantenlo corto y cargado de resultado, con el tono del usuario.

### 6. Quítale el riesgo con una garantía
Escribe una garantía que traslade el riesgo hacia ti. Elige la más fuerte con la que el usuario se sienta cómodo: reembolso incondicional, condicional ("haz el trabajo, si no consigues X, reembolso completo") o una garantía de desempeño ("seguimos trabajando gratis hasta que consigas tu primera venta"). Una garantía específica le gana a una vaga.

### 7. Agrega escasez o urgencia reales
Da una razón para actuar ahora que sea VERDADERA — nunca falsees una cuenta regresiva. Formas legítimas: lugares limitados (solo puedes atender bien a N personas), una fecha de inicio de cohorte, un precio que sube después del lanzamiento, un bono que vence. Escribe la línea exacta.

### 8. Endúlzala con bonos
Agrega de 1 a 3 bonos que resuelvan la *siguiente* objeción después de que digan que sí ("vale, ¿pero cómo retengo a los clientes?"). Cada bono debería sentirse como algo que podría venderse por separado. Ponle nombre a cada uno y dale un valor.

### 9. Escribe la oferta terminada + la línea grand slam
Arma todo en una oferta limpia y lista para presentar, y luego destílala en UNA oración que puedan decir en una llamada o poner en una página:
> "Obtienes [resultado soñado] en [plazo], con [pila principal], respaldado por [garantía] — por [precio]. Solo [escasez]."

## Resultado — guárdalo
Escribe la oferta terminada en `~/offers/<offer-name>.md` (crea la carpeta `~/offers/` si hace falta; convierte el nombre en slug, p. ej. `~/offers/30-day-first-client-system.md`). Confírmale la ruta al usuario. El archivo tiene que contener: el titular del resultado soñado, la tabla de la pila obstáculo→entregable, el nombre, la garantía, la escasez, los bonos, el "valor" total vs el precio y la frase grand slam de una línea.

## Ejemplo (entrada → salida)
**Entrada:** El usuario vende un servicio de "configuración de Notion" de $500 a freelancers. Resultado soñado: "dejar de perderles el rastro a los clientes y los proyectos". Obstáculos: no saben cómo estructurarlo, no tienen tiempo para armarlo, lo intentaron antes y lo abandonaron, tienen miedo de que no se adapte a su forma de trabajar.

**Salida (extracto guardado en `~/offers/freelancer-command-center.md`):**
- **Nombre:** El Centro de Mando del Freelancer
- **Promesa:** Cada cliente, proyecto y fecha límite en un solo panel en 5 días — sin que tengas que construir nada tú.
- **Pila:** Armado de Notion hecho por ti (elimina "no tengo tiempo") + una llamada de personalización de 20 min (elimina "no se va a adaptar a mí") + una checklist operativa diaria de 1 página (elimina "lo voy a abandonar") + un recorrido en video de Loom (elimina "no sé cómo manejarlo").
- **Garantía:** Si no te está ahorrando tiempo en 14 días, lo vuelvo a armar o te devuelvo el dinero.
- **Escasez:** 4 armados al mes para que cada uno sea personalizado.
- **Bono:** Pack de plantillas para la incorporación de clientes.
- **Línea grand slam:** "Ten todo tu negocio freelance funcionando desde un solo panel en 5 días, hecho por ti, con garantía — 4 lugares este mes."

## Notas / casos especiales
- Si el usuario todavía no tiene pruebas, apóyate más en la garantía y en la victoria rápida — sustituyen a una trayectoria.
- No te metas a fondo con el precio aquí; si quieren ayuda para fijar el número, pasa al skill **pricing-calculator**.
- No apiles de más — 3–5 entregables que eliminen cada uno un obstáculo real le ganan a 12 elementos de relleno.
