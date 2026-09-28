---
name: skill-starter
description: Convierte un trabajo que le sigues pidiendo a Claude en tu propio skill reutilizable, para que escribas un solo comando de barra en lugar de volver a explicarlo cada vez. Te entrevista sobre el trabajo, las palabras que realmente usas para pedirlo, los pasos y el archivo que debería guardar — luego escribe un SKILL.md funcional en ~/.claude/skills/ y te dice cómo probarlo. Úsalo cuando el usuario diga "hazme un skill", "convierte esto en un skill", "sigo pidiendo lo mismo", "cómo hago mi propio comando de barra", "construye un skill para esto", "hago esto cada semana, puede Claude simplemente hacerlo", "skill personalizado", "skill starter" o escriba /skill-starter.
---

# Skill Starter — embotella lo que sigues pidiendo

Le has pedido a Claude el mismo tipo de cosa dos o tres veces. Volviste a escribir la misma explicación, obtuviste una respuesta ligeramente distinta cada vez y la arreglaste a mano. Esa es la señal. Un skill congela la buena versión para que la obtengas de la misma forma cada vez, desde un solo comando de barra.

Este es el skill que te convierte en constructor en lugar de consumidor. Todo lo demás en este repo es el trabajo embotellado de otra persona. Este embotella el tuyo.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Comprueba que el disparador sea real
Pregunta: "¿Cuál es el trabajo, y cuántas veces se lo has pedido a Claude?"

- **Menos de dos veces:** diles que esperen. No puedes embotellar un trabajo que todavía no has hecho — estarías adivinando los pasos. Hazlo a mano una vez más y luego vuelve.
- **Dos veces o más:** bien, sigue adelante. Pídeles que peguen uno de los prompts reales que usaron, o que describan la última vez que lo pidieron. Los intentos pasados reales son la mejor materia prima.
- **Es algo único:** dilo claramente y simplemente haz el trabajo en lugar de construir un skill para él.

### 2. Clava el único trabajo
Pídeles que completen esta oración: "Este skill toma ___ y me da ___."

Insiste hasta que ambas mitades sean concretas. "Toma mis notas desordenadas y me da un email de actualización semanal limpio" es un skill. "Ayuda con mi contenido" no lo es.

Luego aplica la Regla de Un Solo Trabajo en voz alta: si la respuesta tiene un "y" en el medio que esconde un segundo trabajo, divídelo. Dos medios skills son peor que uno que funciona. Diles cuál mitad estás construyendo ahora y anota la otra para después.

### 3. Consigue las frases de activación — en sus palabras reales
Esta es la parte que la gente hace mal, así que explica por qué importa: el campo `description` es lo único que lee Claude al decidir si activar el skill. Si está escrito en lenguaje pulido y el usuario escribe lenguaje torpe, el skill se queda ahí y nunca se ejecuta.

Pregunta: "Si necesitaras esto en seis meses y olvidaste que el skill existía, ¿qué escribirías?"

Reúne de cinco a ocho formas de decirlo. Insiste en las descuidadas — las medias oraciones, los errores de tipeo con espíritu, cómo lo dirían a las 11 de la noche. "escribe mi email del lunes", "esa cosa de la actualización semanal", "resume mi semana para el equipo". Incluye también la forma con barra.

### 4. Recorre los pasos
Pídeles que te cuenten cómo harían el trabajo a mano, de principio a fin. Convierte eso en cuatro a siete pasos, cada uno haciendo una sola cosa.

Para cada paso, captura los detalles que hacen bueno el resultado:
- Las preguntas reales que hay que hacerles
- El formato o la plantilla real que hay que llenar
- La comprobación real que dice "esto está bien"

Si no pueden describir un paso, es un paso que Claude tiene que decidir por su cuenta — escribe una regla clara para él en lugar de dejarlo en blanco.

### 5. Decide qué archivo guarda
Todo skill debería terminar con un archivo real en una ruta real. Pregunta: "¿Dónde debería vivir el resultado para que puedas encontrarlo después?"

Elige una ruta razonable bajo `~/` — por ejemplo `~/emails/weekly-update.md` o `~/clients/<name>/brief.md`. La salida del chat desaparece. Un archivo no.

### 6. Escribe el skill
Elige un slug corto en minúsculas con guiones (esto se convierte en su comando de barra). Crea `~/.claude/skills/<slug>/` y escribe `SKILL.md` con esta forma:

```markdown
---
name: <slug>
description: <lo que obtienen, luego las frases de activación entre comillas, separadas por comas, incluido /<slug>>
---

# <Título> — <lema corto>

<2-3 oraciones: el problema, y qué queda al final.>

## Pasos

### 1. <Paso que empieza con verbo>
<Las preguntas reales, la plantilla y las comprobaciones.>

### 2. ...

## Resultado — guárdalo
<Ruta exacta. Contenido exacto. La única siguiente acción.>

## Notas
- <qué hacer cuando la entrada es escasa>
- <el error que esto evita>
```

Escríbelo con su voz usando sus palabras. Luego devuélveles el `description` en voz alta y pregunta: "¿Eso se activaría si escribieras tu propia versión torpe?" Agrega lo que falte.

### 7. Pruébalo
Diles la secuencia exacta:

1. Iniciar una sesión nueva de Claude Code (los skills se cargan al arrancar — un skill escrito a mitad de sesión todavía no está activo).
2. Escribir `/<slug>`.
3. Si se ejecuta, hacer un trabajo real con él y arreglar lo que haya salido mal.

Si `/<slug>` no aparece, el nombre de la carpeta y el campo `name:` no coinciden, o el archivo no está en `~/.claude/skills/<slug>/SKILL.md`. Comprueba ambos.

## Resultado — guárdalo
Escribe `~/.claude/skills/<slug>/SKILL.md`. Muestra el archivo completo en el chat, indica la ruta exacta y da una siguiente acción: "Reinicia Claude Code y escribe `/<slug>` para ejecutarlo de verdad."

## Ejemplo (entrada → salida)
**Entrada:** "Cada viernes le pido a Claude que convierta mis notas desordenadas de la semana en una actualización corta para mis tres clientes. Lo he hecho unas cinco veces y sale distinto cada vez."

**Salida (guardada en `~/.claude/skills/client-update/SKILL.md`):**
```markdown
---
name: client-update
description: Convierte tus notas desordenadas de la semana en un email de actualización para clientes corto y tranquilo que puedes enviar tal cual. Úsalo cuando digas "escribe mi actualización de cliente", "actualización del viernes", "esa cosa del email semanal", "resume la semana para mis clientes", "actualiza a mis clientes" o /client-update.
---

# Client Update — notas del viernes a email listo para enviar

Terminas la semana con notas dispersas y sin energía para escribir tres emails. Esto convierte las notas en una actualización corta por cliente, con una forma que se lee en 20 segundos.

## Pasos

### 1. Consigue las notas
Pide las notas de esta semana, por desordenadas que sean. Si dicen "no escribí ninguna", haz tres preguntas en su lugar: qué se lanzó, qué está atascado, qué sigue.

### 2. Divide por cliente
Clasifica cada línea bajo un nombre de cliente. Todo lo que no encaje con nadie va a una pila de sobrantes y se descarta.

### 3. Escribe cada actualización
Cuatro líneas por cliente, en este orden: qué se hizo, qué sigue, qué necesitas de ellos, una línea de tranquilidad. Sin disculpas. Sin relleno.

### 4. Revisa el tono
Relee cada una. Si suena ansiosa o sobreexplica un retraso, recórtala a una oración tranquila.

## Resultado — guárdalo
Guarda todas las actualizaciones en ~/clients/updates/<date>-updates.md, una por cliente, separadas por una línea. Diles la ruta y que peguen cada una directo en un email.

## Notas
- Notas escasas significan una actualización corta, no una inventada. Nunca inventes progreso.
- Si un cliente tuvo cero actividad, dilo claramente y da una fecha para la próxima actualización real.
```

## Notas / casos especiales
- Los skills solo se cargan al iniciar una sesión. Si el suyo no aparece, esa es casi siempre la razón — reinicia antes de depurar cualquier otra cosa.
- Si el trabajo cambia cada vez, todavía no es un skill. Hazlo a mano hasta que se repita una forma.
- Mantén pequeña la primera versión. Un skill que de verdad ejecutan le gana a uno perfecto que abandonan a mitad de escribirlo.
- Un skill se puede editar en cualquier momento. Diles que arreglen el `SKILL.md` en el momento en que el resultado los decepcione, en lugar de rodearlo en el chat.
- Si el trabajo en realidad es "fijar reglas para un proyecto", eso es **claude-md-builder**, no un skill.
- Si quieren construir el mismo skill para cinco trabajos distintos, ejecuta esto una vez y deja que lo repitan. No lo hagas por lotes — cada entrevista es de donde viene la calidad.
