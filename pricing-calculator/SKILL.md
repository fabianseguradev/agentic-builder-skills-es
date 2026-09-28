---
name: pricing-calculator
description: Fija un precio basado en el valor para tu producto o servicio — con el precio puesto en el resultado que genera para el comprador, no en tus costos ni en tus horas. Cuantifica el valor en dólares para el comprador, ancla 3 niveles (bueno/mejor/el mejor), pone el precio en una fracción del valor entregado, lo pone a prueba contra las objeciones y elige una estructura de pago. Úsalo cuando el usuario diga "cuánto debería cobrar", "qué precio le pongo a esto", "estoy cobrando demasiado poco", "ponle precio a mi oferta", "fija mis tarifas", "esto debería ser una suscripción", o cuando esté a punto de cobrar de menos. Insiste en ejecutarlo siempre que haya que decidir un precio.
---

# Pricing Calculator — pon el precio según el valor, no según el costo

Los fundadores no técnicos casi siempre cobran de menos porque ponen el precio según el esfuerzo ("solo me tomó un fin de semana") en lugar de según el resultado que obtiene el comprador. Este skill le da la vuelta: cuantifica el valor para el comprador y luego cobra una fracción segura de él. El resultado es un precio recomendado, una tabla de 3 niveles y la justificación del valor que el usuario puede decir en voz alta sin titubear.

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia — yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## Pasos

### 1. Cuantifica el resultado en dólares
Toma la oferta + la transformación del perfil y luego pregunta cuánto vale el resultado para el comprador. Encuentra el número usando lo que encaje:
- **Genera dinero:** ¿cuántos ingresos/clientes/ventas les ayuda a conseguir? ("primer cliente = $2,000" o "un panel ahorra 5 h/semana = $X").
- **Ahorra dinero:** ¿qué les evita gastar (una agencia, una herramienta, una contratación)?
- **Ahorra tiempo:** horas ahorradas × lo que vale su tiempo.
- **Evita un dolor:** el costo de que el problema siga sin resolverse (tratos perdidos, estrés, lanzamientos que no ocurren).
Escribe el número honesto de valor, aunque sea un rango conservador. Esto es el ancla de todo.

### 2. Fija el precio como una fracción del valor
Regla general: pon un precio con el que el comprador obtenga un retorno obvio — normalmente **el 10–20% del valor entregado** (es decir, un retorno de 5–10 veces para ellos). Si tu trabajo les ayuda a ganar $10,000, un precio de $1,000–$2,000 es fácil de justificar. Calcula un primer precio a partir del número de valor, no de tus horas.
- Comprueba el piso: tiene que cubrir con holgura tu tiempo y tus costos. Si el precio basado en valor queda por debajo de eso, lo que está mal es la oferta o la audiencia, no el precio — señálalo.

### 3. Ancla tres niveles (bueno / mejor / el mejor)
La gente elige mejor entre opciones que entre sí/no. Construye tres:
- **Bueno** — el resultado central, lo más autogestionado, el precio más bajo. Hace fácil la entrada.
- **Mejor** (el objetivo — la mayoría de los compradores debería caer aquí) — lo central + los entregables que eliminan los obstáculos más grandes (soporte, hecho en conjunto, plazo más rápido). Ponle un precio que lo haga el mejor valor obvio.
- **El mejor** — hecho por ti / 1:1 / acceso premium / garantía. Con un precio alto en parte para que "Mejor" parezca razonable (el ancla).
Diseña "El mejor" para que algunos compradores de verdad lo quieran — no solo como señuelo. Pon el nivel objetivo en el medio y hazlo visualmente el recomendado.

### 4. Ponlo a prueba contra las objeciones
Di en voz alta cada objeción probable y asegúrate de que el precio sobreviva:
- "Es caro" -> reencuadra contra el número de valor y el costo de NO resolverlo.
- "Podría hacerlo yo mismo / conseguirlo más barato" -> ¿cuál es el tiempo, el riesgo y la brecha que realmente están comprando para saltarse?
- "¿Cómo sé que va a funcionar?" -> ¿hay una garantía o una victoria rápida que respalde el precio? (Si no, considera **offer-builder**.)
Si una objeción mata el precio, ajusta el precio O fortalece la oferta — anota cuál.

### 5. Elige la estructura de pago
Ajusta la estructura a cómo aparece el valor:
- **Pago único** — un entregable / una transformación definida con un final.
- **Suscripción / retainer** — valor, acceso o mantenimiento continuos. Lo mejor para ingresos predecibles; necesita valor continuo o las bajas pegan fuerte.
- **Depósito + saldo / plan de pagos** — para precios más altos; reduce la fricción de entrada. Un depósito también filtra a los compradores serios.
Recomienda una, y ofrece una opción de plan de pagos si el precio es lo bastante alto como para asustar a un comprador que encaja bien.

## Resultado — guárdalo
Escribe el resultado en `~/offers/pricing.md` (crea `~/offers/` si hace falta). Incluye: el número de valor para el comprador (con cómo se obtuvo), el precio principal recomendado, la tabla de niveles bueno/mejor/el mejor con lo que incluye cada uno, la estructura de pago recomendada y 2–3 líneas de justificación del valor "para decir en voz alta" que el usuario pueda usar en una llamada. Confírmale la ruta al usuario.

## Ejemplo (entrada → salida)
**Entrada:** El usuario construye asistentes de chat con IA a medida para negocios de servicios locales. Le tomó un fin de semana; iba a cobrar $300.

**Salida (guardada en `~/offers/pricing.md`):**
- **Valor para el comprador:** captura ~10 leads perdidos al mes; cada lead ≈ $150 → ~$1,500/mes, ~$18k/año.
- **Precio recomendado:** $1,500 por la configuración, con el precio en ~10% del valor del primer año.
- **Niveles:** Bueno — configuración del asistente, $1,500. **Mejor (objetivo)** — configuración + 3 meses de ajustes y soporte, $2,500. El mejor — hecho por ti en 2 sucursales + retainer de optimización mensual, $4,000 + $500/mes.
- **Estructura:** pago único para Bueno/Mejor; retainer en El mejor; opción de depósito del 50% en todos.
- **Dilo en voz alta:** "Esto se paga solo el primer mes que atrapa leads que ahora mismo estás perdiendo."

## Notas / casos especiales
- Nunca pongas el precio según tus horas — un proyecto de un fin de semana que le hace ganar $20k al cliente no es un trabajo de $300.
- Si el comprador de verdad no puede obtener mucho valor, es un problema de posicionamiento — mándalos a **positioning-filter** o a una audiencia de más valor.
- Redondea a números seguros ($1,500, no $1,487). Las cuentas raras de costo más margen transmiten amateurismo.
- Para una oferta totalmente nueva sin ninguna prueba, está bien empezar un escalón más abajo para reunir testimonios — dilo de forma explícita y fija el precio "real" al que se va a subir.
