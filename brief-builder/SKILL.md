---
name: brief-builder
description: Convierte un pedido vago en un Brief de 5 Partes quirúrgico que puedes pegar directo en Claude para obtener lo correcto al primer intento. Completa CONTEXTO, OBJETIVO, RESTRICCIONES, FORMATO y LISTO-CUANDO, y luego te da una versión comprimida de una sola oración para pedidos rápidos. Úsalo cuando el usuario diga "escríbeme un prompt", "cómo pido esto", "convierte esto en un prompt", "mejora mi prompt", "no sé cómo describir lo que quiero", "ayúdame a explicarle esto a Claude", "brief para", "qué debería escribir" o "/brief-builder". Úsalo también antes de cualquier proyecto real, para que pidan bien desde la primera vez.
---

# Brief Builder — entra algo vago, sale algo quirúrgico

Los principiantes le piden a Claude "un sitio web" y reciben un sitio web que no es el suyo. La brecha no es de habilidad, es de especificidad. Este skill toma lo que digas, por desordenado que sea, y lo convierte en un Brief de 5 Partes — CONTEXTO, OBJETIVO, RESTRICCIONES, FORMATO, LISTO-CUANDO — que pegas y ejecutas. El mismo marco sirve para una landing page, un email o una hoja de cálculo.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Toma el discurso desordenado y encuentra el entregable
Deja que lo describan con sus propias palabras. No corrijas su lenguaje. Devuélveselo como una sola oración: "Entonces, lo que existe al final es ___ ." Consigue un sí antes de escribir nada.

Si nombraron tres cosas, detente. **Un brief, un entregable.** Elige la que harían primero y anota las demás al final como "próximos briefs".

### 2. Completa CONTEXTO — qué es cierto ahora mismo
Esta es la parte que los principiantes se saltan, y es la razón por la que el resultado se siente genérico. Claude no puede ver su vida. Pregunta solo lo que cambia la respuesta:
- ¿Para quién es? No "para todo el mundo" — una persona que se pueda describir.
- ¿Qué existe ya? Archivos, un sitio, un documento, nada en absoluto.
- ¿Qué saben ellos que Claude no puede adivinar? Su oferta, su precio, la queja real de su audiencia, la herramienta con la que están atados.

Escribe el CONTEXTO en 2-4 oraciones simples de hechos. Nada de objetivos aquí.

### 3. Completa OBJETIVO — lo único que esto debe lograr
Una oración. Empieza con un verbo. Nombra el resultado, no el código.

Elimina estos patrones en cuanto los veas:
- Código en lugar de resultado: "agrega un contenedor flexbox" → "pon las tres tarjetas una al lado de la otra en escritorio".
- Dos objetivos disfrazados de uno: "haz un sitio y escribe mis emails" → divídelo. **Regla de Un Solo Trabajo.**
- Una sensación sin prueba: "hazlo profesional" → "haz que parezca hecho por un consultor de $200/hora, no una plantilla".

### 4. Completa RESTRICCIONES — lo que no puede hacer
Las restricciones son lo que hace que el resultado sea específico. Consigue de 3 a 5. Estimúlalas con:
- Límites de longitud, tamaño o presupuesto.
- Cosas que odian — un tono, un estilo, una palabra, un color.
- Cercas técnicas: un solo archivo, sin registros, que funcione en el celular, sin herramientas de pago.
- Qué dejar fuera por completo.

Si no pueden nombrar ninguna, ofrece dos y deja que reaccionen. La gente es mucho mejor rechazando que inventando.

### 5. Completa FORMATO — la forma de la respuesta
Di exactamente qué se devuelve: un solo archivo `index.html`, una lista de diez viñetas, una tabla de tres columnas, un email de 200 palabras, una carpeta con tres archivos. Incluye dónde debe guardarse si eso importa.

Un formato vago es la razón por la que la gente recibe ensayos cuando quería una lista.

### 6. Completa LISTO-CUANDO — cómo sabes que está terminado
La línea que la mayoría nunca escribe, y la que detiene los retoques infinitos. Tiene que poder comprobarse mirando algo, no sintiéndose satisfecho:
- "Un desconocido en su celular puede leerlo y tocar un botón para enviarme un email."
- "La página carga sin errores y el titular nombra a mi audiencia."
- "La lista tiene diez elementos, ninguno sobre precios."

Si su LISTO-CUANDO contiene "bueno", "bonito" o "profesional", reescríbelo hasta que sea observable.

### 7. Escribe ambas versiones
**Versión larga** — las cinco partes etiquetadas, en un bloque listo para copiar.

**Versión comprimida** — una oración que pueden usar para pedidos pequeños:
> "Dado [contexto], haz [objetivo], sin [restricción], con formato de [formato] — listo cuando [listo-cuando]."

Enseña la línea comprimida de forma explícita. Es la que usarán cuarenta veces a la semana sin abrir este skill.

Luego muestra un breve **antes/después**: su discurso original de un lado, el brief del otro, para que vean qué cambió.

## Resultado — guárdalo
Crea `~/briefs/` si hace falta. Guarda como `~/briefs/<short-slug>.md` — el slug sale del entregable, como `landing-page.md` o `client-welcome-email.md`.

El archivo contiene: el pedido original palabra por palabra, el Brief de 5 Partes en un bloque listo para copiar, la versión comprimida de una línea y cualquier "próximo brief" que haya quedado aparcado.

Diles la ruta y luego la única acción: pegar el bloque de la versión larga en una sesión nueva de Claude y dejar que se ejecute. Si el resultado está mal, cambian UNA parte del brief y lo ejecutan de nuevo — ese es el ciclo, no un fracaso.

## Ejemplo (entrada → salida)

**Entrada:** "Quiero una página para lo de paseo de perros para que la gente me pueda reservar. Nada lujoso."

**Salida (guardada en `~/briefs/dog-walking-page.md`):**

*Antes:* "Quiero una página para lo de paseo de perros para que la gente me pueda reservar."

*Después:*
```
CONTEXTO: Paseo perros en Oakland, sobre todo para gente que trabaja en una
oficina y no puede volver a casa a mediodía. Cobro $28 por paseo. No tengo
sitio web, solo un número de teléfono. Mis clientes me encuentran por los vecinos.

OBJETIVO: Construir una página que haga que un dueño de perro ocupado me
mande un mensaje de texto para reservar un paseo.

RESTRICCIONES: Un solo archivo index.html autocontenido, sin registros, sin
software de reservas. Debe poder leerse en un celular con una mano. Sin fotos
de stock de modelos sonriendo. No mencionar precios de paquetes que todavía
no ofrezco.

FORMATO: Un solo archivo index.html, mobile first, un color de acento, solo
Google Fonts.

LISTO-CUANDO: Un vecino puede abrir el link en su celular, entender en cinco
segundos que paseo perros en Oakland y tocar un botón que abre un mensaje de
texto para mí.
```

*Comprimido:* "Dado que soy un paseador de perros independiente en Oakland sin sitio web, construye un sitio de una página que haga que un dueño ocupado me escriba un mensaje, sin software de reservas ni fotos de stock, como un solo index.html mobile first — listo cuando un vecino pueda tocar un botón para escribirme."

*Próximos briefs:* un volante para la cuadra, un mensaje de seguimiento para clientes recurrentes.

## Notas / casos especiales
- El error que esto evita es pedir un resultado y culpar al modelo por la respuesta. Brief flaco, resultado flaco.
- Si te dan dos oraciones y ningún detalle, no hagas una entrevista. Completa con valores razonables por defecto, márcalos claramente como supuestos al final y deja que corrijan uno. El impulso le gana a un cuestionario.
- Si el entregable es realmente enorme — una app entera, un curso entero — escribe el brief solo para la primera porción que se pueda lanzar y enumera el resto como próximos briefs.
- Nunca pongas código en un brief. Ellos describen el resultado, Claude elige el cómo. Ese es todo el acuerdo.
- Si ya ejecutaron un prompt y obtuvieron algo malo, no lo reescribas desde cero — pasa a **prompt-fixer**, que primero diagnostica por qué falló.
