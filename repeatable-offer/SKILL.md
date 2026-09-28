---
name: repeatable-offer
description: Offer-builder hace que una oferta sea irresistible. Este hace que tu servicio sea repetible, para que dejes de cotizar desde cero cada vez que alguien pregunta cuánto cuesta. Encuentra la parte de tu trabajo que es igual en cada proyecto, y la envuelve en un nombre fijo, un alcance fijo, un precio fijo, un plazo fijo y una checklist de entrega que sigues igual en cada pedido. Úsalo cuando el usuario diga "haz esto repetible", "sigo haciendo esto a medida para todos", "empaqueta lo que hago", "convierte mi servicio en un producto", "estoy cotizando cada trabajo desde cero", "productiza mi servicio", "estoy atrapado cambiando tiempo por dinero" o "/repeatable-offer".
---

# Repeatable Offer: vende la misma cosa dos veces

El trabajo a medida agota porque cada venta empieza en cero. Vuelves a explicar qué haces, adivinas un precio y luego el proyecto crece más allá de lo acordado. La solución es encontrar la parte del trabajo que es igual en cada proyecto, ponerle un marco y vender ese marco una y otra vez. Eso es lo que significa "productizar": convertir un servicio en algo con bordes, como una cosa en un estante.

El resultado es una oferta de una página que puedes enviarle a un comprador y que también puedes seguir tú mismo mientras entregas.

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize**. O simplemente dime tu nombre, nicho, oferta y audiencia, y yo lo creo.
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil, para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario. Usa solo lo que está en el perfil, o pregunta.

## Pasos

### 1. Encuentra el núcleo repetible
Pídeles que repasen las últimas 2 o 3 veces que hicieron este trabajo, proyecto por proyecto. Luego busca qué fue igual todas las veces. Eso es el 80% que se repite sin importar quién sea el cliente, y es el producto real. El resto es ruido que se siente importante porque fue distinto.

Dos preguntas hacen la mayor parte del trabajo:
- "¿Qué haces en cada uno de estos, sin importar para quién sea?"
- "¿Qué es lo que al cliente realmente le importa al final?"

Escribe el núcleo en una oración: "Tomo [insumo] y lo convierto en [resultado]." Si todavía no pueden terminar esa oración, sigue preguntando sobre los últimos trabajos. No sigas adelante con un núcleo vago, porque todo lo que viene después se construye sobre él.

### 2. Define un entregable fijo
Ahora reemplaza "depende" por una cosa concreta que recibe el comprador. Consultoría no es un entregable. Un sitio web construido, un set de cinco posts, una automatización que funciona más un recorrido en video: esos son entregables, porque puedes señalarlos.

- Escribe exactamente qué reciben, como una lista corta de viñetas.
- Escribe cómo se ve "terminado", para que ambas partes sepan cuándo acabó.

Esa línea de meta importa más de lo que parece. La mayor parte del dolor del trabajo a medida viene de que nadie acordó cuándo terminó el proyecto.

### 3. Fija un plazo fijo
Un producto tiene un tiempo de entrega. Dale uno y dilo claramente: "entregado en 7 días", "un sprint de 2 semanas", "en línea dentro de 48 horas".

Elige el límite realista más generoso, no el mejor caso. Un plazo que superas te hace ver bien, y un plazo que no cumples te cuesta la referencia. El plazo también es un punto de venta por sí solo, porque la mayoría de la gente que compra servicios no tiene idea de cuándo va a recibir algo.

### 4. Traza el marco alrededor del alcance
Este es el paso difícil y el que la gente se salta. Escribe qué NO está incluido. El desbordamiento de alcance es cuando un trabajo crece en silencio más allá de lo acordado, y es lo que convierte un producto de vuelta en trabajo a medida.

- Nombra los pedidos a los que vas a decir que no.
- Limita las variables con números reales: "hasta 5 páginas", "una ronda de revisión", "una sola plataforma".
- Toma los extras que la gente sigue pidiendo y conviértelos en complementos con nombre y precio propio. Un complemento pagado es un sí. Un extra gratis es una fuga.

Termina con tres listas simples: incluido, no incluido, complementos con precios.

### 5. Ponle nombre y precio
Dale un nombre que diga el resultado, no el proceso. "Rescate de Bandeja de Entrada" le gana a "Paquete de Consultoría en Automatización". Manténlo lo bastante corto como para decirlo en voz alta.

Luego escribe la promesa de una línea: "Obtienes [entregable] en [plazo], hecho por ti."

Luego ponle un número fijo. Pon el precio según lo que vale el resultado para el comprador, no según cuántas horas te toma, porque las horas te castigan por volverte más rápido. Si están atascados con el número, pasa a **pricing-calculator**. Si quieren apilar esto en una oferta más grande y más difícil de rechazar con una garantía y bonos, eso es **offer-builder** después de esto.

### 6. Elige cómo se entrega
Cumplimiento solo significa cómo se hace y se entrega realmente el trabajo. Elige uno:

- **Hazlo tú mismo.** Compran plantillas o una herramienta y la ejecutan ellos. El más barato de entregar, el que más escala.
- **Hazlo contigo.** Tienes un proceso fijo y llamadas donde los guías. Repetible, más contacto, precio más alto.
- **Hecho por ti.** Ejecutas tu proceso fijo en su nombre. El precio más alto, y limitas tus cupos para que la calidad se sostenga.

Luego escribe los pasos estándar de entrega, la misma checklist que sigues en cada pedido: recepción, construcción, revisión, entrega. Esta checklist es la parte que lo hace repetible en la vida real y no solo en papel. También es lo que le entregarías a la primera persona que contrates.

## Resultado: guárdalo
Escribe la oferta de una página en `~/offers/<product-name>.md` (crea `~/offers/` si hace falta, y convierte el nombre en un nombre de archivo, así "Rescate de Bandeja de Entrada" se convierte en `inbox-rescue.md`).

El archivo contiene: la oración del núcleo repetible, la especificación del entregable, el plazo, las listas de incluido, no incluido y complementos, el nombre más la promesa de una línea más el precio, el modelo de cumplimiento y la checklist de entrega.

Diles la ruta y luego da una siguiente acción: enviarle la promesa de una línea a una persona que encaje, y ver qué pregunta. Las preguntas que hacen son las partes del marco que todavía no están claras.

## Ejemplo (entrada → salida)
**Entrada:** "Hago ayuda freelance de automatización. Cada trabajo es distinto, cotizo de memoria y el trabajo siempre crece."

**Salida (guardada en `~/offers/inbox-rescue.md`):**
- **Núcleo repetible:** Tomo la recepción de leads desordenada de una pequeña empresa y la convierto en un solo flujo automático.
- **Entregable:** un formulario de recepción conectado, que alimenta un CRM (la herramienta que guarda los contactos de clientes), más una respuesta automática a cada lead nuevo, más un breve recorrido en video.
- **Terminado significa:** entra un lead de prueba y recibe una respuesta sin que nadie lo toque.
- **Plazo:** en línea en 5 días hábiles.
- **Incluido:** una fuente de recepción, un CRM, una secuencia de respuesta automática.
- **No incluido:** código a medida, más de una marca, cambios continuos después de la entrega.
- **Complementos:** secuencia de respuesta extra $200. Segunda sede $400.
- **Nombre, promesa, precio:** "Rescate de Bandeja de Entrada. Tus leads capturados y respondidos automáticamente en 5 días, hecho por ti. $1,200."
- **Cumplimiento:** hecho por ti, 4 cupos al mes.
- **Checklist de entrega:** llamada de recepción, mapear su flujo actual, construirlo, probar con leads de muestra, recorrido y entrega.

## Notas / casos especiales
- Si nada se repite entre sus últimos trabajos, todavía no están listos para productizar todo este servicio. Elijan el único pedido que reciben más seguido y armen el marco de ese primero. Un producto estrecho le gana a uno flexible que nunca se vende dos veces.
- Resiste la tentación de hacer que el producto haga de todo. Una oferta aburrida, estrecha y repetible vende más que una a medida ingeniosa, porque un comprador la entiende en diez segundos.
- Si solo han hecho esto una vez, están adivinando el núcleo. Hagan el próximo trabajo, tomen notas de lo que realmente hicieron y ejecuten esto de nuevo con material real.
- La página de una sola cara terminada cumple doble función. Es la página de ventas que le envías a los compradores, y es la checklist que sigues mientras entregas, así que ambas partes del trabajo se mantienen iguales cada vez.
- Revísala después de cinco pedidos. Para entonces vas a saber qué complemento compra siempre la gente, y ese normalmente pertenece dentro del marco a un precio más alto.
