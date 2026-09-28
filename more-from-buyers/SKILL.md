---
name: more-from-buyers
description: Encuentra de 3 a 5 formas concretas de ganar más dinero con los clientes que ya tienes, sin más tráfico, más seguidores ni una audiencia más grande. Mira la única cosa que vendes ahora y ordena los movimientos por esfuerzo, primero el dinero más fácil. Úsalo cuando el usuario diga "cómo gano más dinero con lo que tengo", "audita mi oferta", "estoy dejando dinero sobre la mesa", "debería subir mi precio", "agregar un upsell", "cómo agrego ingresos recurrentes", "mi oferta solo genera dinero una vez" o "/more-from-buyers".
---

# More From Buyers: el dinero está detrás de la venta

La mayoría de la gente que quiere más ingresos sale a buscar más personas, así que empuja más fuerte con los posts y el tráfico. Esa es la forma cara. El dinero más barato suele estar detrás de una venta que ya estás haciendo: un precio demasiado bajo, un pequeño complemento que nadie ofreció, un siguiente paso que nadie propuso.

Este skill mira la única cosa que vendes hoy y te da de 3 a 5 movimientos específicos, ordenados para que el dinero más fácil vaya primero.

## Lee esto antes de ejecutarlo
Este skill necesita una oferta que ya se esté vendiendo. No hacen falta muchas ventas. Un puñado basta. Trabaja a partir de lo que los compradores reales hicieron de verdad, así que sin ventas no hay nada que auditar y simplemente inventaría cosas.

Compruébalo con el usuario en el primer mensaje. Si todavía no han vendido nada, díselo claramente y mándalos al lugar correcto en su lugar:
- Todavía no tienen una oferta por escrito, o no pueden decirla en una oración: ejecuta primero **offer-builder**.
- La oferta existe pero no saben cuánto cobrar: ejecuta primero **pricing-calculator**.

Ambos son gratis y están en este repo. Dilo con amabilidad y sin convertirlo en un fracaso. Conseguir la primera venta es un trabajo distinto de sacarle más al comprador, y hacerlos en el orden equivocado desperdicia una noche.

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia, y yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario. Usa solo lo que está en el perfil, o pregunta.

## Pasos

### 1. Consigue la foto actual
Haz estas seis preguntas. Mantenlo conversacional y no sueltes las seis de una vez si el usuario está respondiendo con oraciones completas.

1. ¿Qué vendes y cuánto cobras? (la única cosa principal)
2. ¿Es un pago único, o se cobra cada mes?
3. ¿Más o menos cuántas vendes al mes? Si es mensual, ¿la gente se queda o se va?
4. ¿Qué pasa justo después de que alguien compra? ¿Le ofreces algo más, o nada?
5. Cuando alguien dice que no, ¿qué suele decir? ("demasiado caro", "ahora no", "prefiero que lo hagas tú por mí")
6. ¿Qué obtiene realmente el comprador, y cuánto vale eso para él en dinero o en horas ahorradas?

La respuesta 6 es la que la gente se salta, y es la que decide el movimiento de precio. Insiste en un número real o en una cantidad real de tiempo.

### 2. Devuélveles el modelo actual en una línea
Algo como: "Auditoría única de $300, unas 15 al mes, no se ofrece nada después, así que unos $4,500 al mes." Haz que lo confirmen. Si no pueden confirmar los números, usa rangos y di que son aproximados.

### 3. Pasa la oferta por las seis palancas
Toma cada una y decide si es una oportunidad real para *esta* oferta. Sáltate las que no encajan. Forzar las seis es como terminas dando consejos genéricos.

- **Subir el precio.** Si el resultado vale mucho más de lo que cobran, el precio es demasiado bajo. Las señales: nadie se queja nunca del precio, casi todos dicen que sí, los compradores parecen encantados. Propón un número nuevo específico y la razón que lo justifica.
- **Order bump.** Un complemento pequeño y barato ofrecido en el momento del pago. "¿Agregas X por $Y?" Piensa en lo que naturalmente acompaña a la cosa principal. Requiere poco esfuerzo y es casi pura ganancia.
- **Upsell.** Una oferta relacionada más grande que se muestra justo después de comprar, cuando la confianza está en su punto más alto. "Ya tienes X. ¿Quieres que también haga Z, o que me encargue de todo por ti?" ¿Cuál es el siguiente nivel obvio?
- **Downsell.** Una versión más pequeña o más barata para la gente que quería entrar pero para la que el sí era demasiado grande. Un plan de pagos cuenta. Esto convierte algunos no en síes más pequeños en lugar de nada.
- **Algo recurrente.** Convertir una venta única en dinero que llega cada mes: un plan de soporte, revisiones periódicas, una membresía mensual o una tarifa fija mensual por estar disponible. Para una oferta de pago único, normalmente es la palanca más grande que existe.
- **Retener compradores por más tiempo.** Solo si ya cobran mensualmente. Arreglar que la gente se vaya es más barato que encontrar gente nueva. Usa sus respuestas a la 3 y la 5 y propón un arreglo concreto, como una mejor primera semana o una victoria temprana rápida.

### 4. Elige los 3 a 5 más fuertes y haz que cada uno sea específico
Para cada movimiento, di exactamente qué agregar, más o menos cuánto cobrar y la única línea que usarían para proponerlo. "Agrega un upsell" no es un movimiento. "Después de la auditoría, ofrece hacer el arreglo por $1,500" es un movimiento.

### 5. Ordena por esfuerzo, primero el dinero más fácil
Clasifícalos en tres grupos para que sepan qué hacer esta noche y qué puede esperar:

- **Esta semana.** Normalmente el cambio de precio, el order bump, el downsell. Son sobre todo una decisión más una oración, sin nada que construir.
- **Este mes.** El upsell, o un complemento recurrente simple.
- **Este trimestre.** Una capa completa de membresía o tarifa mensual, un nivel premium, un sistema para retener a la gente.

Para cada movimiento escribe: el movimiento, cómo implementarlo, el impacto probable y el nivel de esfuerzo.

Sobre el impacto, sé orientativo y honesto. "Más o menos un 20 a 30% más en cada venta" está bien. Una cifra precisa inventada, no. Nunca afirmes como un hecho lo que un cambio va a generar.

### 6. Agrega un nivel premium si encaja
Una versión hecha por ti o VIP a un precio mucho más alto. Aunque casi nadie la compre, hace que la oferta principal parezca razonable a su lado, y atrapa a los compradores que quieren lo mejor. Esboza qué incluye y un precio.

### 7. Comprueba que de verdad puedan entregarlo
Antes de entregar la lista, mírala como carga de trabajo. Si dos de los movimientos los enterrarían en un trabajo de entrega que no pueden hacer, dilo y marca cuál hacer primero. El dinero que arruina la entrega cuesta más de lo que genera.

## Guarda el resultado
Escribe la auditoría en `~/offers/more-from-buyers-<offer-slug>-<YYYY-MM-DD>.md` (crea `~/offers/` si hace falta). La fecha va en el nombre a propósito, para que volver a ejecutar esto dentro de unos meses no sobrescriba la anterior.

El archivo contiene: el modelo actual en una línea, los movimientos ordenados con la implementación, el impacto y el esfuerzo de cada uno, la idea del nivel premium y cualquier advertencia sobre la entrega del paso 7.

Diles la ruta y luego da una siguiente acción: hacer esta semana el primer movimiento de "esta semana". Ofrece escribir el texto real del movimiento que elijan, la línea del bump, el pitch del upsell o el email del downsell.

## Ejemplo (entrada → salida)
**Entrada:** "Vendo una auditoría de sitio web de pago único de $300 a pequeñas tiendas en línea. Unas 15 al mes. Después de que compran no les ofrezco nada. La gente que dice que no suele decir que preferiría que yo mismo arreglara las cosas. La auditoría normalmente encuentra problemas que les cuestan miles en ventas perdidas."

**Salida (extracto, guardado en `~/offers/more-from-buyers-website-audit-2026-08-08.md`):**

> **Modelo actual:** Auditoría única de $300, unas 15 al mes, no se ofrece nada después, unos $4,500 al mes.
>
> **1. Sube el precio a $500. Esta semana.**
> Encuentras miles en ventas perdidas por $300 y nadie se queja. Impacto: unos $3,000 más al mes con el mismo volumen. Esfuerzo: cambiar un número.
>
> **2. Ofrece hacer el arreglo por $1,500. Esta semana.**
> Tus no literalmente están pidiendo esto. Ofrécelo a todos, compren la auditoría o no. Impacto: incluso 3 al mes son otros $4,500. Esfuerzo: escribir una oferta.
>
> **3. Order bump: entrega en 48 horas por $100. Esta semana.**
> Una casilla en el pago. Impacto: casi pura ganancia con quizás un tercio de los compradores. Esfuerzo: una línea.
>
> **4. Monitoreo mensual por $200 al mes. Este mes.**
> Revisiones continuas después del arreglo. Convierte a un comprador de una sola vez en dinero cada mes. Impacto: la palanca de largo plazo más grande aquí. Esfuerzo: decidir qué les envías cada mes.
>
> **Nivel premium:** Revisión completa más 90 días de trabajo conjunto por $4,000. Hace que la auditoría de $500 parezca pequeña y atrapa a las tiendas que quieren que se encarguen de todo de principio a fin.

## Notas / casos especiales
- Todo el punto es sacarle más a los clientes que ya tienes. Si el instinto del usuario es "necesito más tráfico", tráelo de vuelta aquí primero. Venderle más a la gente que ya compró es más barato que encontrar gente nueva.
- No fuerces las seis palancas. Tres movimientos que encajan con esta oferta le ganan a seis que encajan con cualquier oferta.
- El precio lo deciden ellos. Recomienda un número y el razonamiento, y luego deja que lo fijen.
- Si le venden a empresas, la palanca del precio suele ser más grande de lo que creen. Si le venden a personas, suele serlo la recurrente.
- Si han vendido menos de unas cinco, ejecútalo igual pero limita los movimientos al precio y a un complemento. Todavía no hay suficiente patrón como para construir todo un conjunto de ofertas extra.
- Vuelve a esto cada pocos meses. El movimiento correcto con 15 ventas al mes no es el correcto con 50.
