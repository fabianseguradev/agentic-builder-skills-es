---
name: sales-page
description: Construye una página que parece un producto real y que de verdad lo vende — problema, estado posterior, qué es, qué incluye, prueba, precio dicho una vez, garantía, preguntas frecuentes y un botón repetido a lo largo de la página. Pone todo en el orden que hace que la gente compre en lugar del orden en que se te ocurra escribirlo. Úsalo cuando el usuario diga "/sales-page", "constrúyeme una página de ventas", "una página para vender mi cosa", "necesito una página para mi curso", "escribe mi página de ventas", "página de producto", "página de pago para mi oferta", "una página que venda", "cómo vendo esto en línea" o "la gente me sigue pidiendo un link para comprar".
---

# Sales Page — el orden es la oferta

La mayoría de las primeras páginas de ventas fallan por el orden, no por las palabras. Abren con el producto, te golpean con un precio antes de que quieras algo y entierran la prueba al final. Esto construye la página en la secuencia que de verdad funciona: hacerlos sentir el problema, mostrarles el después, luego decir qué es, qué incluye, quién más lo consiguió, y solo entonces cuánto cuesta.

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia — yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## Pasos

### 1. Comprueba que la oferta sea sólida antes de construirle una página
Una buena página no puede salvar una oferta difusa. Dos comprobaciones rápidas:

- **¿Tienen un precio?** Si no, detente y pasa a **pricing-calculator**, luego vuelve. Construir una página de ventas alrededor de "ya voy a pensar el número después" desperdicia la sesión.
- **¿Pueden decir en una oración para quién es y qué cambia?** Si esa oración sale blanda — "es como un tipo de coaching para cualquiera que quiera crecer" — detente y pasa a **offer-builder**. Vuelve con una oferta real.

Si ambas están bien, sigue adelante.

### 2. Reúne la materia prima
Pide esto. Mantén las preguntas cortas y agrupadas.

- **El problema que sienten.** No el problema que tú diagnosticas — el que se quejarían a un amigo a las 11 de la noche. Sus palabras.
- **El estado posterior.** Qué es cierto 90 días después de que esto funcione. Específico y observable, no "más seguro de sí mismo".
- **Qué es.** El sustantivo simple. Un programa de 6 semanas. Un pack de plantillas de 40 páginas. Una llamada de una hora más un plan escrito.
- **Qué incluye.** Cada componente, como una lista. Sesiones, archivos, acceso, soporte, plazos.
- **Prueba.** Testimonios reales, resultados reales, credenciales reales, capturas reales. Lo que realmente tengan. Si no tienen nada, dilo — vas a usar otro tipo de prueba en el paso 3 en lugar de inventar una.
- **El precio**, y si hay un plan de pagos.
- **La garantía**, o su política honesta de reembolsos. "Sin reembolsos, y esta es la razón" está permitido y le gana a una promesa falsa.
- **Las tres principales objeciones.** Demasiado caro, no tengo tiempo, esto va a funcionar para alguien como yo, esta persona es legítima, ya compré cosas así antes y no las terminé.

### 3. Escribe la página en este orden exacto — nunca lo reordenes
Escribe todo el texto antes de tocar la construcción. Con su voz. Oraciones cortas, concretas, sin exageración.

1. **El problema que sienten.** Abre aquí. Dos o tres líneas que les hagan pensar "ese soy yo". Si no se sienten vistos en los primeros cinco segundos, nada de lo que sigue importa.
2. **El estado posterior.** Pinta qué cambia, de forma específica. Esto es lo que están comprando — no tu producto.
3. **Qué es.** Una línea clara que nombra la cosa. Ahora que quieren el resultado, diles el vehículo.
4. **Qué incluye.** Una lista fácil de escanear. Cada elemento dice qué hace por ellos, no solo qué es: "Seis llamadas de 45 minutos — para que nunca estés atascado más de una semana."
5. **Prueba.** Testimonios con nombres reales si los tienen. Si no tienen testimonios, usa en su lugar prueba del trabajo: su propio antes y después, el proceso mostrado con honestidad, cuánto tiempo llevan haciendo esto, una muestra del material real. Nunca escribas una cita falsa ni inventes un número.
6. **El precio — dicho una vez, claramente.** Un número, una línea de plan de pagos si la hay, sin teatro de anclaje, sin descuentos falsos. Dilo limpio y sigue adelante. Aparece exactamente una vez en la página.
7. **La garantía.** Quita el riesgo justo después del número, donde ocurre el titubeo.
8. **Preguntas frecuentes que eliminan las tres principales objeciones.** Una pregunta cada una, respondida directo y corto. Responde la objeción, no la esquives.
9. **Una última línea corta y el botón.**

La regla que hay que decir en voz alta: **nunca pongas el precio antes del valor.** Si un precio aparece antes de que quieran el resultado, es solo un número y siempre es demasiado grande.

### 4. Un botón, tres veces
Un solo llamado a la acción, las mismas palabras, el mismo color, en tres lugares a lo largo de la página:
- Justo después del estado posterior, para quien ya está convencido.
- Justo después de la prueba.
- Al final de todo, después de las preguntas frecuentes.

La misma etiqueta cada vez — el botón es una promesa, no un espectáculo de variedades. "Únete por $297" o "Consigue el pack de plantillas." No "Enviar", no "Saber más".

¿Adónde lleva? Su link de pago existente (Stripe, Gumroad, Lemon Squeezy, PayPal), o un link de reservas, o un link de email si venden por conversación. Pregunta cuál tienen. Si no tienen ninguno, usa un link mailto con un asunto prellenado para que puedan seguir vendiendo hoy, y anota en el archivo dónde va la URL de pago real más adelante.

### 5. Construye la página
Un solo `index.html` autocontenido:
- Sin herramientas de build, sin librerías de JavaScript externas. Solo Google Fonts — una fuente display, una fuente para el cuerpo, que encajen con su marca.
- Un color de acento más neutros. El acento le pertenece al botón y a nada más. Nunca el degradado de IA de morado a azul.
- Animación solo con transforms y opacity, con moderación. Sin desenfoque ni ruido animados, sin marquesinas que se desplazan solas. Sin cuentas regresivas.
- Totalmente legible con JavaScript desactivado. Mobile first — la mayoría de las páginas de ventas se leen en un teléfono en la cama.
- Tipografía de página larga: interlineado generoso, ancho de lectura cómodo (unos 65 caracteres), separaciones de sección claras para que se pueda escanear rápido.
- El texto real del paso 3, nunca lorem ipsum. Íconos SVG en línea. Fotos solo si las aportaron o de una URL gratuita de Unsplash que aprobaron.

Guarda en `~/sites/<slug>/index.html`.

### 6. Previsualiza, haz el ciclo y luego la prueba de leer en voz alta
Ábrelo:

```bash
open ~/sites/<slug>/index.html
```

Pídeles que lo lean en voz alta, de principio a fin. Todo con lo que tropiecen, lo reescriben. Todo lo que les dé vergüenza de sí mismos suele ser exageración y hay que quitarlo.

Luego haz el ciclo en palabras simples, de 5 a 10 rondas. Dos comprobaciones para repetir cada un par de rondas:
- ¿El precio aparece exactamente una vez, y después del valor?
- ¿Hay algo en esta página además del único botón?

Escribe `~/sites/<slug>/NOTES.md` con la oferta, el precio, las tres objeciones, el destino de pago y el siguiente paso.

## Resultado — guárdalo
- `~/sites/<slug>/index.html` — la página de ventas completa, un archivo.
- `~/sites/<slug>/NOTES.md` — la oferta en una línea, el precio, las tres objeciones manejadas, adónde apunta el botón y el siguiente paso de mañana.

Indica ambas rutas. Única siguiente acción: ejecutar **deploy-it**, y luego mandarle el link a tres personas que ya dijeron que estaban interesadas.

## Ejemplo (entrada → salida)
**Entrada:** "Acompaño a diseñadores freelance nuevos. Son 6 semanas, llamadas grupales, $497. Han pasado 4 personas y dos de ellas consiguieron clientes."

**Salida (guardada en `~/sites/designer-coaching/index.html`, en orden):**

- **Problema:** "Eres bueno en el trabajo. Simplemente no tienes idea de cómo lograr que alguien te pague por él — así que sigues rehaciendo tu portafolio en lugar de mandar el email."
- **Después:** "Dentro de seis semanas habrás mandado 30 pitches reales, tenido al menos tres conversaciones y sabrás exactamente qué decir cuando alguien pregunte tu tarifa."
- **Qué es:** "Un programa grupal de 6 semanas para diseñadores que consiguen sus primeros clientes que pagan."
- **Incluye:** "Seis llamadas grupales de 90 minutos — para que nunca estés atascado más de una semana." Más la plantilla de pitch, el guion de tarifas, un hilo privado para feedback.
- **Prueba:** dos testimonios con nombre de los dos que consiguieron clientes, presentados como dos de cuatro — honesto, no inflado.
- **Precio:** "$497, o dos pagos de $260." Dicho una vez.
- **Garantía:** "Ven a las dos primeras llamadas. Si no es para ti, mándame un email y te devuelvo todo."
- **Preguntas frecuentes:** "Tengo un trabajo de tiempo completo — ¿puedo hacer esto?" / "¿Y si no tengo portafolio?" / "¿Por qué debería confiar en ti?"
- Botón **"Únete por $497"** tres veces, apuntando a su link de Stripe.

## Notas / casos especiales
- El error que esto evita: escribir la página en el orden en que piensa el vendedor (aquí está mi cosa, aquí está el precio, por favor compra) en lugar del orden en que lo siente el comprador (este es mi problema, esa es la vida que quiero, ah, eso es lo que cuesta).
- Si no tienen ninguna prueba, no la falsees. Muestra el trabajo en sí, sé honesto sobre que están empezando y considera un precio de fundador más bajo — esa honestidad convierte mejor que una cita inventada.
- Si quieren una cuenta regresiva o escasez falsa, di que no. Si la fecha límite es real, plantéala como una oración simple.
- Si la página se alarga y les da pánico, es normal — largo está bien cuando cada sección hace un trabajo. Corta las secciones que no lo hacen, no las oraciones que sí.
- Derivación: **pricing-calculator** si no hay un número. **offer-builder** si la oferta en sí es débil. **objection-handler** si las respuestas de las preguntas frecuentes siguen saliendo defensivas. **deploy-it** para publicar.
