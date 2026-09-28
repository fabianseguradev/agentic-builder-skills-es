---
name: warm-outreach
description: Construye una lista de contacto priorizada de tu red cálida y un primer mensaje genuino y de baja presión para que consigas tu primer cliente entre personas que YA te conocen y confían en ti — antes de siquiera tocar la prospección en frío. Actívalo siempre que el usuario diga "a quién debería contactar", "necesito mi primer cliente", "prospección cálida", "haz una lista de contacto", "a quién ya conozco", "ayúdame a empezar a vender", "no sé con quién hablar" o "cómo consigo mi primer cliente sin sonar vendedor".
---

# Warm Outreach — empieza con gente que ya confía en ti

El primer cliente más rápido casi nunca viene de desconocidos. Viene de alguien que ya te conoce: un cliente anterior, un excolega, alguien de una comunidad en la que estás, una persona que le dio like a tus últimos tres posts. Este skill te ayuda a volcar toda esa red en papel, ordenarla y escribir un primer mensaje que abra una conversación en lugar de lanzarle un pitch a un amigo.

Todo el punto es **cálido antes que frío, y honesto antes que insistente.** No le estás mandando spam a nadie. Estás hablando con personas reales a las que te alegraría escuchar de vuelta.

## Personalización
Este skill trabaja con *tu* voz de marca. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nombre, nicho, oferta y audiencia — yo lo creo).
- Si falta un campo que este skill necesita, haré una o dos preguntas rápidas y guardaré las respuestas en el perfil para que solo tengas que responder una vez.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## Pasos

### 1. Vuelca toda la red (todavía sin filtrar)
Pídele al usuario que enumere a todos los que ya lo conocen, en grupos sueltos — acepta respuestas desordenadas y a medio recordar. Estimula cada grupo para que no se traben:
- **Clientes pasados y actuales** — cualquiera que alguna vez les pagó, aunque haya sido una vez, aunque haya sido hace años.
- **Colegas e historial laboral** — exjefes, compañeros de trabajo, gente de trabajos anteriores.
- **Comunidad y pares** — gente de cualquier grupo, cohorte, Slack/Discord, mastermind o curso en el que estén.
- **DMs cálidos y redes sociales** — gente que responde a sus posts, les manda DM, o con quien chatean en línea.
- **Amigos y personal** — cualquiera que atendería su llamada, que podría conocer a alguien aunque ellos mismos no sean el comprador.

Diles: todavía no juzguen si encaja, solo anoten nombres. Apunten a 20–40. Si se traban, pregunta "¿quiénes fueron las últimas 10 personas a las que le escribiste?" y "¿en los posts de quién comentas?"

### 2. Puntúa a cada persona del 1 al 3
Para cada nombre, puntúa dos cosas rápidas:
- **Encaje** — qué tan probable es que esta persona (o alguien que conoce) de verdad quiera la oferta del usuario. (3 = encaja claro, 2 = quizás/cercano, 1 = comprador improbable pero un buen conector.)
- **Calidez** — qué tan fuerte es la relación ahora mismo. (3 = respondería en menos de una hora, 2 = amigable pero en silencio últimamente, 1 = perdimos el contacto.)

Ordena por encaje + calidez combinados. Lo más alto de la lista (encaje alto Y calidez alta) es a quien le escriben primero. La gente de encaje bajo pero calidez alta no está desperdiciada — son **conectores** a los que les piden una referencia, no una venta.

### 3. Escribe 3 variaciones de apertura
Usando la voz de marca, escribe **tres** aperturas de primer contacto que el usuario pueda adaptar por persona. Reglas que evitan que suene a venta:
- **Empieza por ellos, no por el pitch.** Haz referencia a algo real — su trabajo, un momento compartido, por qué les vino a la mente. Sin oferta en el primer mensaje salvo que sea genuinamente natural.
- **Pregunta, no anuncies.** Termina con una pregunta ligera fácil de responder, para que inicie una conversación.
- **Sin urgencia falsa, sin bombardeo de halagos, sin gancho de "pregunta rápida".** Que suene al usuario escribiéndole a alguien que respeta.

Haz que las tres sean distintas para que distintas relaciones reciban el registro correcto:
1. **Reconectar** — para alguien con quien perdieron el contacto (calidez 1–2). Puro ponerse al día, cero pitch.
2. **Señal suave** — para una persona cálida y relevante (encaje 2–3). Menciona qué están construyendo ahora y pregunta si les resulta relevante.
3. **Pedido de referencia** — para un conector (encaje bajo, calidez alta). Pregunta a quién podrían conocer, no si *ellos* lo quieren.

Cada apertura debería tener un espacio `[entre corchetes]` para el único detalle personal que el usuario completa por persona — ese detalle es lo que hace que no sea una plantilla.

### 4. Guarda el archivo
Escribe todo en `~/warm-outreach-list.md`:
- La tabla ordenada (Nombre | Grupo | Encaje | Calidez | Primer movimiento).
- Las tres variaciones de apertura con sus espacios de personalización entre corchetes.
- Una línea corta de "empieza aquí" que nombre a las 5 personas principales a las que escribirle primero esta semana.

Confirma la ruta y dile al usuario: escríbeles a los 5 principales hoy, personaliza un detalle en cada uno, y no mandes más de un puñado al día — esto es una conversación, no una campaña.

## Ejemplo de entrada → salida
**Entrada:** El usuario ejecuta el skill. Oferta (del perfil): "Construyo automatizaciones simples de incorporación de clientes para contadores, configuración de $500." Vuelcan 24 nombres.

**Salida — `~/warm-outreach-list.md` (extracto):**

| Nombre | Grupo | Encaje | Calidez | Primer movimiento |
|---|---|---|---|---|
| Dana R. | Cliente anterior | 3 | 3 | Señal suave (escribir primero) |
| Marcus (excolega) | Colega | 2 | 3 | Reconectar → señal suave |
| Priya, grupo de contabilidad | Comunidad | 3 | 2 | Señal suave |
| Tío Tom | Personal | 1 | 3 | Pedido de referencia |

**Apertura de señal suave:**
> hola Dana — justo estaba pensando en [el lío que desenredamos con tus formularios de admisión el año pasado]. últimamente he estado construyendo pequeñas automatizaciones que resuelven exactamente ese tipo de trabajo tedioso de incorporación para contadores. sin pitch, solo curiosidad — ¿sigue siendo la incorporación de clientes un dolor de cabeza de tu lado?

**Empieza aquí:** Dana, Priya, Marcus, y dos más — 5 mensajes esta semana, un detalle personal cada uno.

## Notas / casos especiales
- Si el usuario casi no tiene red, eso es real — llévalo hacia el ángulo de "conectores" (aperturas de referencia) y hacia una comunidad cálida en la que ya esté, en lugar de empujarlo a lo frío antes de que esté listo.
- Nunca escribas una apertura que tergiverse la relación o fabrique un recuerdo compartido. Si el usuario no puede llenar el `[corchete]`, la persona no es lo bastante cálida para la versión de señal suave — usa reconectar en su lugar.
- Mantén el lote pequeño. Una lista enorme enviada toda de una vez se lee como spam masivo y mata la calidez. Los 5 principales primero.
- Combina naturalmente con el skill **dm-writer** cuando quieran redactar por completo el mensaje para una persona específica.
