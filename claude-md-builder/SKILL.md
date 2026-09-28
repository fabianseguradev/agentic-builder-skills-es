---
name: claude-md-builder
description: Construye el archivo de memoria CLAUDE.md de un proyecto para que Claude deje de olvidar tus reglas cada vez que abres una sesión nueva. Te entrevista sobre qué es el proyecto, las reglas que siempre hay que seguir, lo que nunca hay que hacer, dónde viven los archivos y cómo quieres que te hablen — y luego escribe un CLAUDE.md corto en la carpeta del proyecto. Úsalo cuando el usuario diga "haz un CLAUDE.md", "claude md builder", "configura la memoria del proyecto", "Claude sigue olvidando cosas", "cómo dejo de repetirle lo mismo a Claude", "Claude olvida qué es mi proyecto", "dale reglas a Claude para este proyecto", "archivo claude.md", "quad md" o escriba /claude-md-builder.
---

# CLAUDE.md Builder — dale a Claude una memoria para este proyecto

En cada sesión nueva, Claude empieza en blanco. Vuelves a explicar el proyecto, vuelves a enunciar tus reglas y lo ves cometer el mismo error que cometió ayer. Un archivo `CLAUDE.md` lo resuelve: vive en la carpeta del proyecto y se lee al inicio de cada sesión. Este skill te entrevista y escribe uno corto y preciso.

Lo corto es todo el punto. Un `CLAUDE.md` es un centro de mando, no una autobiografía. Cada línea que agregas compite por atención con todas las demás. Un archivo inflado hace que Claude funcione peor, no mejor — las reglas que importan quedan enterradas bajo las que no.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Encuentra el proyecto y revisa qué existe ya
Ejecuta `pwd` para confirmar la carpeta actual y lista lo que contiene para poder describirle el proyecto al usuario con precisión. Revisa si ya existe un `CLAUDE.md` aquí.

- Si existe uno, léelo y dile al usuario que lo vas a reescribir, mostrando qué vas a conservar. Nunca lo sobrescribas en silencio.
- Si la carpeta parece vacía o no relacionada con un proyecto, haz una pregunta: "¿En qué carpeta está este proyecto?" No adivines.

Dile al usuario en una línea lo que ves: "Esto parece un proyecto de landing page — un index.html y una carpeta de imágenes. ¿Es correcto?"

### 2. Entrevista — seis preguntas, una a la vez
Hazlas una a la vez y espera cada respuesta. Las respuestas cortas están bien — tú las vas a afinar.

1. **¿Qué es este proyecto, en una oración?** ("Una página de reservas para mi negocio de paseo de perros.")
2. **¿Para quién es y qué es lo único que tiene que hacer?** (Este es el objetivo que zanja las discusiones más adelante.)
3. **¿Cuáles son las reglas que quieres que Claude siga todas y cada una de las veces?** Dales ejemplos para estimularlos: mantenerlo en un solo archivo, mostrarme siempre una vista previa antes de cambiar algo, nunca agregar páginas nuevas sin preguntar, usar mis colores.
4. **¿Qué no debería hacer Claude nunca?** Ejemplos para estimularlos: nunca borrar archivos, nunca agregar un sistema de login, nunca instalar nada, nunca cambiar los textos sin preguntar.
5. **¿Dónde viven las cosas?** Qué archivo es el real, dónde están las imágenes, qué ignorar. Si no lo saben, mira la carpeta y propónlo tú.
6. **¿Cómo quieres que te hablen?** Lenguaje simple, sin mostrar código salvo que lo pidan, explicar las decisiones en una línea, preguntar antes de los cambios grandes.

Si una respuesta es vaga, haz una pregunta para afinarla, no cinco. "Usa mis colores" se convierte en "¿Qué colores? Pega los códigos hex o descríbelos."

### 3. Recórtalo antes de escribirlo
Este es el paso que la gente se salta. En voz alta, aplica tres recortes:

- **Quita todo lo que Claude haría de todos modos.** "Escribe código limpio" y "sé útil" son líneas desperdiciadas. Conserva solo las reglas que cambian el comportamiento.
- **Quita todo lo que es cierto hoy pero no el mes que viene.** Las listas de tareas y los pendientes no van aquí. Para eso está un registro de construcción.
- **Quita los duplicados.** Si dos reglas dicen lo mismo, conserva la más precisa.

Meta: menos de 40 líneas. Si es más largo, recorta otra vez. Dile al usuario qué recortaste y por qué, en una línea cada cosa.

### 4. Escribe CLAUDE.md
Escribe en `CLAUDE.md` dentro de la carpeta del proyecto, con esta forma:

```markdown
# <Nombre del proyecto>

<Una oración: qué es esto y para quién es.>

## El objetivo
<Lo único que este proyecto debe lograr. Úsalo para zanjar cualquier duda sobre el alcance.>

## Siempre
- <regla>
- <regla>

## Nunca
- <regla>
- <regla>

## Dónde viven las cosas
- `<archivo>` — <qué es>
- `<carpeta>` — <qué es>

## Cómo hablarme
- <preferencia>
- <preferencia>
```

Usa sus palabras, no las tuyas. Si dijeron "no lo hagas elegante", escribe eso, no "mantener la sobriedad visual".

### 5. Demuestra que funcionó
Un archivo de memoria que no puedes verificar es un archivo de memoria en el que no vas a confiar. Dile al usuario exactamente cómo probarlo:

1. Cierra esta sesión y empieza una nueva en esta carpeta.
2. Escribe: "¿Qué es este proyecto y cuáles son mis reglas?"
3. Claude debería responder a partir del archivo sin que tú expliques nada.

Si no lo hace, el archivo está en la carpeta equivocada — Claude lee `CLAUDE.md` de la carpeta en la que iniciaste la sesión. Diles que comprueben que abrieron Claude Code en la carpeta del proyecto.

### 6. Diles cómo hacerlo crecer
Una nota corta: cuando corrijan a Claude dos veces sobre lo mismo, esa corrección se convierte en una línea de `CLAUDE.md`. No antes. El archivo crece a partir de errores reales, no de imaginar reglas por adelantado.

## Resultado — guárdalo
Escribe `CLAUDE.md` en la carpeta actual del proyecto (la del paso 1). Muéstrale al usuario el archivo completo en el chat, indica la ruta exacta y dale una siguiente acción: "Empieza una sesión nueva aquí y pregunta '¿cuáles son mis reglas?' para demostrar que se cargó."

## Ejemplo (entrada → salida)
**Entrada:** El usuario tiene una carpeta con un sitio de una página para su negocio de paseo de perros. Tiene que volver a explicar una y otra vez que debe seguir siendo un solo archivo y que Claude nunca debe tocar los textos de precios.

**Salida (guardada en `./CLAUDE.md`):**
```markdown
# Página de reservas de Paws & Co.

Un sitio de una página donde los dueños de perros de mi barrio reservan un paseo. Hecho primero para celulares.

## El objetivo
Llevar a un desconocido desde la parte superior de la página hasta un formulario de reserva completado en menos de 30 segundos.

## Siempre
- Mantener todo en un solo archivo: index.html. Los estilos y los scripts van en línea.
- Mostrarme la página en el navegador antes de dar algo por terminado.
- Preguntar antes de cambiar cualquier texto de precios. Esos números están fijos.

## Nunca
- Nunca agregar una segunda página.
- Nunca instalar nada ni agregar una librería.
- Nunca usar texto de relleno genérico — escribir textos reales o pedírmelos.

## Dónde viven las cosas
- `index.html` — todo el sitio. Es el único archivo que importa.
- `photos/` — mis fotos de perros. Usar estas, no descargar nuevas.

## Cómo hablarme
- Lenguaje simple. No mostrarme código salvo que lo pida.
- Una línea sobre por qué tomaste una decisión, y seguir adelante.
```

## Notas / casos especiales
- El error número uno es un `CLAUDE.md` que se lee como un diario. Si el usuario sigue agregando, recuérdale: cada línea extra hace que las líneas importantes se escuchen menos.
- Si el usuario todavía no tiene un proyecto, no escribas un archivo vacío. Dile que ejecute **plan-first** y vuelva cuando haya algo que describir.
- Las reglas que solo aplican a una tarea van en el prompt, no en el archivo de memoria. La memoria es para las cosas que son ciertas en cada sesión.
- Si quieren reglas que apliquen a todos los proyectos de su máquina, ese es otro archivo: `~/.claude/CLAUDE.md`. Menciónalo una vez, no lo construyas aquí.
- Cuando una regla se ignora una y otra vez, normalmente es demasiado vaga. Reescríbela como algo comprobable: "nunca agregues una página" le gana a "mantenlo simple".
