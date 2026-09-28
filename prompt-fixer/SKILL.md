---
name: prompt-fixer
description: Pega el prompt que te dio un mal resultado y recibe la razón por la que falló más el prompt reescrito para ejecutar en su lugar. Revisa las siete causas habituales — demasiado vago, tres pedidos en uno, sin restricciones, sin formato, sin listo-cuando, falta de contexto, pedir código en lugar de un resultado — y te entrega una versión arreglada. Úsalo cuando el usuario diga "esto no es lo que quería", "Claude me dio basura", "mi prompt no funcionó", "arregla mi prompt", "por qué hizo eso", "ignoró lo que le pedí", "me sigue dando lo que no es", "reescribe este prompt" o "/prompt-fixer".
---

# Prompt Fixer — diagnostica y luego reescribe

Pediste algo, recibiste algo equivocado, y se siente como si el modelo te hubiera fallado. Casi siempre es un prompt flaco, no un mal modelo. Este skill encuentra cuál de siete cosas faltó, te lo dice en una línea y te devuelve un prompt reescrito que puedes ejecutar ahora mismo.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Reúne la evidencia
Pide el prompt que usaron, palabra por palabra. Si todavía lo tienen, toma también lo que devolvió — aunque sea un resumen como "hizo una landing page con degradado morado y testimonios falsos".

Haz también una pregunta: "¿Qué querías realmente en su lugar?" Una oración. Ese es el blanco al que apunta la reescritura.

Si solo tienen el prompt y no el resultado, sigue adelante. El diagnóstico normalmente aparece en el prompt solo.

### 2. Di primero lo tranquilizador, una vez
Empieza con: "Esto es un problema del prompt, no un problema tuyo. Nada está roto y nada se desperdició." Dilo una vez, claramente, y luego ponte a trabajar. Los principiantes abandonan justo en este momento, y abandonan porque creen que son malos para esto.

### 3. Haz las siete revisiones
Pasa las siete sobre su prompt. Marca cada una como acierto o fallo. No te detengas en la primera — la mayoría de los malos prompts tienen dos o tres.

1. **Demasiado vago.** ¿Podrían cinco personas distintas leer esto e imaginar cinco resultados distintos? "Hazme un sitio web" falla. La señal: ninguna persona que se pueda describir, ningún resultado que se pueda describir.
2. **Tres pedidos en uno.** Cuenta los verbos que producen algo. Más de un entregable significa que se viola la **Regla de Un Solo Trabajo**, y Claude hace todos a media profundidad. "Construye la página y escribe mis emails y configura mi dominio" son tres prompts.
3. **Sin restricciones.** Nada dijo lo que no puede hacer. Sin cercas, el resultado se desliza hacia el promedio de todo — el degradado morado genérico, los testimonios falsos, el aspecto de foto de stock. La falta de restricciones es la causa más común de "parece hecho por una IA".
4. **Sin formato.** No dijeron la forma de la respuesta, así que recibieron un ensayo cuando querían una lista, o cinco archivos cuando querían uno.
5. **Sin listo-cuando.** No hay línea de meta, así que el resultado se detiene donde al modelo le pareció, y no pueden saber si está bien.
6. **Falta contexto que Claude no podía saber.** Su precio, la queja real de su audiencia, lo que ya existe en su máquina, lo que intentaron la semana pasada. Claude no puede ver nada de eso. Esta es la causa cuando el resultado es técnicamente correcto pero se siente como el negocio de otra persona.
7. **Pidieron código en lugar de un resultado.** Escribieron "agrega un flexbox con una media query" o "usa React". Son directores, no mecanógrafos — describir la maquinaria limita el resultado a lo que ellos casualmente saben. El arreglo siempre es: describe lo que una persona debería ver o poder hacer.

### 4. Nombra la causa principal
Elige LA que hizo más daño y dila en una sola oración, en su lenguaje, ligada a lo que realmente recibieron. "Te salieron testimonios falsos porque nada en tu prompt le dijo qué es realmente tu negocio — eso es falta de contexto."

Enumera las causas secundarias como viñetas cortas debajo. No des una clase sobre las siete.

### 5. Reescríbelo
Produce el prompt arreglado en un bloque listo para copiar, usando la forma de 5 Partes: CONTEXTO, OBJETIVO, RESTRICCIONES, FORMATO, LISTO-CUANDO.

Reglas para la reescritura:
- Usa sus palabras reales y sus detalles reales siempre que los hayan dado.
- Donde tuviste que suponer, supón con sensatez y márcalo como supuesto debajo del bloque — nunca inventes números, ingresos, clientes ni credenciales.
- Si el original eran tres pedidos, reescribe solo el primero y enumera los otros dos como prompts separados para ejecutar después.
- Nunca pongas código en la reescritura.

### 6. Muestra la diferencia en palabras simples
Dos o tres líneas: qué agregaste y por qué va a cambiar el resultado. "Agregué una restricción contra los degradados y las fotos de stock — solo eso mata el aspecto de IA. Agregué un listo-cuando para que sepas cuándo parar."

Esta es la parte que enseña. La próxima vez escribirán bien el prompt ellos solos, que es el verdadero objetivo.

## Resultado — guárdalo
Crea `~/briefs/` si hace falta. Guarda como `~/briefs/fixed-<short-slug>.md`.

El archivo contiene: el prompt original palabra por palabra, lo que recibieron, la causa principal en una línea, las causas secundarias, el prompt reescrito en un bloque listo para copiar, los supuestos asumidos y la diferencia en palabras simples.

Diles la ruta y luego la única acción: empezar una sesión **nueva** de Claude y pegar el prompt reescrito. Ejecutar un arreglo encima de una mala conversación arrastra con él la respuesta equivocada anterior.

## Ejemplo (entrada → salida)

**Entrada:** "Escribí 'constrúyeme una landing page para mi negocio de coaching' y me hizo una página con un degradado morado, tres reseñas falsas de cinco estrellas de gente que no existe y una tabla de precios con tres niveles que nunca mencioné."

**Salida (guardada en `~/briefs/fixed-coaching-landing-page.md`):**

**Causa principal:** Falta de contexto. Nunca le dijiste qué es realmente tu coaching ni quién lo compra, así que llenó los huecos con una plantilla genérica — de ahí salieron las reseñas inventadas y los niveles de precio imaginarios.

**Además:** Sin restricciones (nada prohibía degradados, pruebas falsas ni precios). Sin listo-cuando. Sin formato.

**Reescrito:**
```
CONTEXTO: Acompaño a gerentes de marketing recién despedidos durante sus
primeros 90 días como freelance. Una oferta: un programa 1:1 de 6 semanas.
Todavía no tengo testimonios. No tengo logo. Mis clientes me encuentran en LinkedIn.

OBJETIVO: Construir una página que haga que un gerente de marketing despedido
agende conmigo una llamada introductoria gratuita.

RESTRICCIONES: Un solo index.html autocontenido. Sin testimonios, sin reseñas,
sin logos, sin tabla de precios — no tengo ninguna de esas cosas y no las voy a
falsear. Sin degradados morados ni azules. Un color de acento. Mobile first.

FORMATO: Un solo archivo index.html. Solo Google Fonts, una fuente display y
una fuente para el cuerpo.

LISTO-CUANDO: Alguien en su teléfono puede leerla en 30 segundos, saber que es
para marketers despedidos y tocar un botón para agendar una llamada.
```

**Supuestos:** que la llamada introductoria es gratuita y que el botón debería llevar a un calendario. Cambia cualquiera de los dos si no es así.

**Qué cambió:** El contexto real reemplazó a la plantilla. Una restricción que prohíbe las pruebas falsas significa que no puede volver a inventar reseñas. Un listo-cuando significa que sabrás cuándo dejar de editar.

## Notas / casos especiales
- El error que esto evita es que un principiante concluya "la IA no puede hacer esto" después de un solo prompt flaco. Da el diagnóstico con calidez y pasa rápido a la reescritura.
- Si no recuerdan el prompt exacto, trabaja a partir de lo que recibieron — la forma de una respuesta equivocada revela lo que faltaba.
- Si el prompt en realidad está bien y el resultado era solo un primer borrador, dilo y diles que reaccionen en palabras simples y lo ejecuten de nuevo. De cinco a diez rondas es lo normal — ese es el Ciclo de Construcción, no un prompt roto.
- Si están atascados en un mensaje de error en lugar de un mal resultado, es otro problema — pasa a **error-decoder**.
- Si están empezando desde cero en lugar de reparar algo, pasa a **brief-builder**.
