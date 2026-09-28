---
name: fable-goal
description: Convierte una descripción divagante de un resultado deseado en un prompt /goal pulido y autónomo para Fable. Úsalo siempre que el usuario diga /fable-goal, "convierte esto en un prompt de goal", "escríbeme un prompt para fable", "quiero que fable construya X, escribe el prompt", o divague sobre algo que quiere que se haga y pida el prompt que lo haga realidad. El resultado es un único prompt para copiar y pegar, no la construcción en sí. NO lo uses cuando el usuario quiere que la cosa se construya ahora mismo en esta sesión; solo cuando quiere el PROMPT que la hará realidad en una sesión nueva.
---

# Fable Goal Prompt Writer

Convierte la divagación del usuario en un prompt /goal excepcional que pueda pegar en una sesión nueva de Fable. No estás construyendo la cosa. Estás diseñando el prompt que construye la cosa.

## La filosofía

La idea central: **quítate del camino del modelo.** Fable es lo bastante inteligente como para hacer casi cualquier cosa si el prompt (1) articula el deseo con claridad, (2) le da herramientas y (3) le da una forma de verificar su propio trabajo. Un gran prompt /goal no microgestiona el cómo. Clava el qué, concede libertad creativa explícita en la ejecución y exige autoverificación antes de terminar.

El ejemplo de referencia que define el género: "Quiero construir 25 sitios web con Fable para demostrar sus capacidades extremas... tienes total libertad creativa... alójalos en Netlify y pásame el link... haz al menos tres pasadas de iteración antes de dar por bueno cada sitio... 25 sitios web alojados en Netlify con rutas /guide y tres pasadas de iteración es tu /goal. Trabaja de forma completamente autónoma y no me pidas nada hasta que hayas terminado todo."

## Opcional: el perfil de marca

Si el usuario tiene un perfil de marca guardado — un `brand.md` junto a este skill, o un perfil personal en su configuración global (`~/.claude/CLAUDE.md` o `~/.claude/brand-profile.md`) — léelo una vez al inicio de la ejecución. Ahí viven sus valores por defecto permanentes: pruebas y números de audiencia, sistema de diseño de la casa y rutas de recursos, destinos por defecto para los resultados, reglas de voz y qué MCPs/herramientas suele usar. Trae SOLO las entradas que la tarea realmente toca.

Si no existe ningún perfil, no pasa nada — trata cada dato de marca como un hueco que llenas preguntando (mira el paso 2) o dejando que el mandato de descubrimiento lo cubra. El skill funciona en frío; un perfil solo elimina las preguntas.

## Proceso

### 1. Extrae lo que la divagación ya contiene

La gente piensa en fragmentos, sobre todo al dictar por voz. Interpreta la intención por encima de las palabras literales (términos mal transcritos como "Quad MD" significan CLAUDE.md, "Netlefi" significa Netlify). Extrae: el entregable, la cantidad, la audiencia o el propósito, cualquier herramienta que hayan nombrado, cualquier nivel de calidad que hayan insinuado y dónde deberían quedar los resultados.

### 2. Llena los huecos con valores por defecto; pregunta solo cuando importe

Sintetiza tú mismo los huecos pequeños, usando el perfil de marca si existe. Haz una pregunta SOLO cuando la respuesta cambiaría el prompt de forma significativa. Las cosas sobre las que vale la pena preguntar:

- **Resultado** — si de verdad no puedes saber cuál es el entregable
- **Escala** — si la cantidad cambia la forma del trabajo (5 vs 50) y nada la insinúa
- **Destino** — si no puedes deducir dónde deben quedar los resultados (link alojado, carpeta local, post publicado, archivo guardado)
- **Recursos** — si la tarea necesita un insumo específico que el usuario no te ha dado (un logo, una imagen de referencia, colores de marca, un archivo fuente) y ningún perfil de marca lo aporta, pídelo
- **Datos de marca** — si el resultado es público y no hay un perfil del que sacar pruebas, audiencia o un sistema de diseño, pide el uno o los dos que suben el nivel de calidad

Si preguntas, haz todas las preguntas en UN solo lote de AskUserQuestion y luego escribe el prompt. Nunca entrevistes por rondas. Si la divagación (más cualquier perfil) cubre lo básico, no preguntes nada y anota tus supuestos en su lugar.

**Verifica antes de nombrar.** Un prompt de goal que apunta a un skill, una ruta o un MCP que no existe manda a la sesión nueva a una búsqueda sin salida. Antes de escribir el prompt, dedica 30 segundos a confirmar los recursos específicos que planeas nombrar: haz `ls` de las rutas de archivo, comprueba que el skill existe, echa un vistazo a la lista de herramientas disponibles para el MCP. El entorno en vivo es la fuente de verdad, no el perfil. Nombra solo lo que verificaste Y lo que sostiene peso en esta tarea (normalmente 2-4 cosas). Todo lo demás, incluido cualquier cosa que falte o sea incierta, es trabajo del mandato de descubrimiento: el prompt le dice a Fable que encuentre o averigüe lo que necesita.

### 3. Escribe el prompt usando esta anatomía

Todo prompt /goal tiene siete partes, entretejidas como prosa natural y fluida (no encabezados, no una especificación con viñetas). En primera persona, como el usuario hablándole a Fable:

1. **Deseo + lo que está en juego.** Qué quieren y por qué importa. Entregable concreto, cantidad concreta. Si lo va a ver una audiencia, dilo con el número real. Lo que está en juego hace que el modelo se esfuerce más.
2. **Nivel de calidad.** Cómo se ve lo excelente para esta tarea, en una o dos oraciones. Los adjetivos vívidos le ganan a las especificaciones ("animaciones de otro mundo, paletas de colores excepcionales").
3. **Inventario de herramientas + mandato de descubrimiento.** Nombra las herramientas, MCPs, rutas de archivo y claves específicas que tendrá la sesión (solo las que verificaste que existen), esboza un flujo de trabajo de ejemplo como sugerencia y luego suéltalo de inmediato: "puedes lograr esto de muchas formas". Después concede el descubrimiento: dile a la sesión que se espera que vaya a BUSCAR lo que necesite en lugar de trabajar de memoria o quedarse corta. Eso significa buscar en la web referencias de diseño y buenas prácticas actuales, usar librerías, repos, fuentes o kits de componentes de código abierto cuando le ganen a hacerlo a mano, descargar o generar recursos, y hacer un inventario de sus propias herramientas disponibles al inicio de la ejecución para saber con qué está trabajando. Una oración como "antes de empezar, haz un inventario de las herramientas y MCPs que realmente tienes, y ve a buscar o descargar cualquier referencia, librería o recurso que necesites en el camino; tienes internet a tu disposición" convierte una sesión que adivina en una sesión que busca.
4. **Libertad creativa + concesión de autoridad para decidir.** Permiso explícito para desviarse, elegir flujos de trabajo y "mostrar de lo que es capaz". Esta es la cláusula de quitarse del camino; nunca te la saltes. También cubre las herramientas: cualquier herramienta nombrada en el prompt es una sugerencia, y la sesión debería cambiarla por una mejor si la encuentra. Si el usuario quiere que la sesión tome las decisiones, dilo: cada decisión de criterio que surja a mitad de la ejecución (nombres, estilo, límites del alcance, costos de oportunidad) la decide la sesión con buen gusto, sin devolvérsela al usuario.
5. **Ciclo de verificación.** Cómo comprueba el modelo su propio trabajo antes de dar algo por terminado. Por defecto: al menos tres pasadas de iteración, donde una pasada significa volver a recorrer el resultado terminado con lupa buscando problemas y oportunidades de mejora. Adapta la verificación al medio (renderiza y mira el video, carga la página y recórrela haciendo clic, ejecuta el script con datos reales).
6. **Entrega.** Exactamente dónde quedan los resultados y qué se devuelve (el link, la ruta del archivo, la URL del post).
7. **La línea del goal + directiva de autonomía.** Cierra reformulando el entregable en una sola oración: "[X con Y y Z] es tu /goal. Trabaja de forma completamente autónoma y no me pidas nada hasta que hayas terminado todo." Para trabajos grandes que se pueden paralelizar, agrega un empujón para usar subagentes/flujos de trabajo en paralelo.

Longitud objetivo: 150-350 palabras. Lo bastante largo como para cargar lo que está en juego, las herramientas y la verificación; lo bastante corto como para que nada diluya la línea del goal.

### 4. Entrega

Entrega el prompt en un único bloque de código cercado para que se copie limpio. Debajo, agrega una breve lista de **Supuestos** (2-4 viñetas como máximo) que cubra los huecos que llenaste, para que el usuario pueda corregir cualquier cosa con una línea en lugar de volver a divagar. Nada más. Sin preámbulo encima del bloque de código.

## Ejemplo

**Divagación:** "Quiero como 5 landing pages distintas para lo de mi pack de prompts gratis, que se vean todas totalmente diferentes y locamente buenas, súbelas a algún lado donde pueda verlas"

**Salida:**

```
Quiero que construyas 5 landing pages para mi pack de prompts gratis, cada una fundamentalmente distinta de las demás, como forma de mostrarme el rango más fuerte posible de direcciones antes de que elija una. Las va a ver mi audiencia, así que el nivel es alto: tipografía excepcional, diseños impactantes y movimiento que se sienta diseñado y no de plantilla. Cada página necesita un titular, prueba y un único CTA de captura de email para el pack de prompts. Tienes total libertad creativa sobre la dirección visual de cada una. Puedes generar cualquier imagen que necesites con las herramientas de imagen que tengas disponibles, y puedes lograr esto de muchas formas usando muchos flujos de trabajo, así que antes de empezar, haz un inventario de las herramientas y MCPs que realmente tienes, ve a buscar o descargar cualquier referencia, librería o recurso que necesites en el camino, y muéstrame de lo que eres capaz. Antes de dar por buena cada página, haz al menos tres pasadas de iteración: vuelve a recorrer la página en vivo con lupa buscando problemas de diseño y oportunidades para mejorarla y complejizarla. Paraleliza entre subagentes para que las páginas se desarrollen de forma independiente. Cuando las 5 estén listas, despliégalas en Netlify y pásame los 5 links con una descripción de una línea de cada dirección. 5 landing pages del pack de prompts fundamentalmente distintas, en línea en Netlify con tres pasadas de iteración cada una, es tu /goal. Trabaja de forma completamente autónoma y no me pidas nada hasta que hayas terminado todo.
```

**Supuestos:**
- El CTA es de captura de email para el pack de prompts (sin conectar automatización de marketing, ya que son candidatas para revisión, no páginas en producción)
- Netlify como hosting ya que dijiste "súbelas a algún lado"
- Cada página recibe una dirección visual distinta para que veas todo el rango antes de comprometerte
```
