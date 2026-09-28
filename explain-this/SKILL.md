---
name: explain-this
description: Pega cualquier archivo, listado de carpeta, fragmento, configuración o línea que no entiendas y recibe una explicación en lenguaje simple a nivel de principiante total — qué es, qué hace, por qué existe y qué pasaría si desapareciera. Termina con la única cosa que vale la pena entender y la única cosa que puedes ignorar tranquilo. Úsalo cuando el usuario diga "qué es este archivo", "explícame esto", "qué hace esto", "qué estoy mirando", "no entiendo mi proyecto", "qué es package.json", "por qué hay tantos archivos", "esto es importante", "puedo borrar esto", "explícame mi carpeta" o "/explain-this".
---

# Explain This — haz que tu propio proyecto deje de dar miedo

La carpeta de tu proyecto se llena de archivos que nunca pediste y que no reconoces, y empieza a sentirse como la máquina de otra persona. Pega aquí cualquier parte y recibe una explicación simple: qué es, qué hace, por qué está ahí y si alguna vez lo tocarías. El objetivo no es convertirte en programador. Es que te sientas cómodo en tu propio proyecto.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Toma lo que peguen
Acepta cualquier cosa: un archivo entero, un listado de carpeta, cinco líneas de código, una configuración, un error, una sola palabra que vieron. Si nombran una ruta en lugar de pegar, lee el archivo tú mismo.

Si pegan algo enorme, no expliques cada línea. Explica el trabajo del archivo y luego las tres o cuatro partes que de verdad les importan. Una explicación línea por línea de un archivo de 400 líneas no enseña nada.

Si pegan algo sin ninguna pregunta, asume que la pregunta es "qué es esto y debería importarme".

### 2. Responde las cinco preguntas, en este orden
Siempre estas cinco, siempre cortas. Encabezados, no párrafos.

- **Qué es.** La categoría, en una frase. "Un archivo de configuración." "Una lista de las herramientas externas que toma prestadas tu proyecto." "La página real que ve la gente."
- **Qué hace.** El trabajo que realiza mientras el proyecto funciona, en una o dos oraciones. Usa una comparación cotidiana solo si es realmente precisa — una mala metáfora es peor que ninguna.
- **Por qué existe.** Quién o qué lo puso aquí y qué lo pidió. Los principiantes suponen que cada archivo fue una decisión suya. La mayoría no lo fue — lo creó una herramienta. Dilo, porque es un alivio.
- **Qué pasa si desapareciera.** Sé específico y honesto. "Nada, es una caché y se vuelve a generar." "El sitio deja de cargar por completo." "Tus estilos desaparecen pero el texto se queda." Esta es la pregunta que de verdad están haciendo cuando preguntan si un archivo es importante.
- **Qué cambiarías de verdad aquí.** Señala las dos o tres líneas o valores que alguien que no programa editaría de forma realista — el título, el color, el texto, el link. Di que el resto es maquinaria.

### 3. Ajusta bien el nivel de principiante
Reglas para toda la explicación:
- Define un término técnico en una frase corta la primera vez que aparezca y luego úsalo con normalidad. No lo definas dos veces.
- Nunca digas "simplemente", "solo" u "obviamente".
- Lo concreto antes que lo general. "Esta línea define el título de la pestaña que ves arriba en el navegador" le gana a "esto maneja los metadatos".
- Sáltate todo lo que es cierto pero no les sirve. No necesitan saber qué es un bundler para hacer funcionar su sitio.
- Nunca insinúes que deberían aprender a escribir esto. Ellos son los directores.

### 4. Señala lo que merezca una señal
Solo cuando aplique, una línea cada una:
- Algo aquí es un secreto — una clave, una contraseña, un token — y no debería publicarse ni pegarse en un chat.
- Este archivo se genera automáticamente, así que si lo editas a mano se sobrescribe.
- Este archivo se puede borrar sin problema y volverá solo.
- Este archivo es el que más importa de toda la carpeta.

### 5. Cierra con las dos líneas
Termina cada explicación con exactamente dos líneas, etiquetadas:

- **Vale la pena entender:** la única idea de aquí que va a rendir en cada proyecto futuro. No lo más complejo — lo más útil. "Cada página que construyes tiene un `<head>` para el navegador y un `<body>` para el humano."
- **Puedes ignorar:** la única cosa que deberían dejar de mirar. Dales permiso explícitamente. "Nunca necesitas abrir node_modules. Jamás. Son solo herramientas descargadas."

Dos líneas, no más. Esa es la conclusión que de verdad van a conservar.

## Resultado — guárdalo
Crea `~/claude-explained/` si hace falta. Guarda como `~/claude-explained/<name>.md`, con el nombre de lo que preguntaron — `package-json.md`, `my-project-folder.md`, `index-html.md`.

El archivo contiene: lo que pegaron (recortado si es enorme), las cinco respuestas, cualquier señal y las dos líneas de cierre.

Diles la ruta y luego la única acción: nada que hacer. Este es para leer. Dilo claramente para que no se queden esperando una tarea.

Menciona una vez que la carpeta se convierte en su glosario personal, con sus propias palabras, sobre su propio proyecto.

## Ejemplo (entrada → salida)

**Entrada:** "Hay un archivo llamado package.json en mi carpeta que nunca hice. ¿Se supone que tengo que saber qué es? ¿Puedo borrarlo?"

**Salida (guardada en `~/claude-explained/package-json.md`):**

**Qué es:** El documento de identidad de tu proyecto. Una lista corta que dice cómo se llama tu proyecto y qué herramientas externas toma prestadas.

**Qué hace:** Cuando tú o Claude inician tu proyecto, la computadora lee primero este archivo para saber qué hay que cargar. También guarda comandos abreviados — por eso funciona escribir `npm run dev`.

**Por qué existe:** No lo hiciste tú. Una herramienta lo creó automáticamente la primera vez que se configuró tu proyecto. Casi todos los proyectos del mundo tienen uno.

**Si desapareciera:** Tu proyecto dejaría de funcionar. No sabría qué cargar ni qué significan los comandos abreviados. Así que no, no lo borres — pero es fácil de recrear si alguna vez lo hicieras.

**Qué cambiarías de verdad aquí:** Siendo realistas, una línea: `"name"`. Es el nombre de tu proyecto. La sección `"scripts"` lista tus comandos abreviados, así que vale la pena echarle un vistazo para ver qué puedes escribir. Todo lo que está bajo `"dependencies"` lo manejan las herramientas — déjalo en paz y deja que Claude lo edite.

**Vale la pena entender:** Tu proyecto toma prestadas herramientas de otras personas en lugar de construirlo todo desde cero, y este archivo es la lista de préstamos. Eso es cierto para cada proyecto que hagas.

**Puedes ignorar:** Los números de versión con los símbolos `^`. Nunca vas a necesitar pensar en ellos.

## Notas / casos especiales
- El error que esto evita es que un principiante se sienta como un turista en su propia carpeta y nunca vuelva a abrirla. La comodidad es el entregable.
- Si pegan algo que contiene un secreto real — una API key, una contraseña — dilo de inmediato, antes de explicar cualquier otra cosa, y diles que traten esa clave como expuesta.
- Si pegan algo que de verdad no es importante, dilo en la primera línea. No escribas cinco secciones sobre un archivo lock para parecer exhaustivo.
- Si el archivo es enorme y generado, explica la categoría una vez y diles que nadie lee estos archivos, ni siquiera los profesionales.
- Si están pegando un error en lugar de un archivo, pasa a **error-decoder** — ese les da una oración para arreglarlo, este solo explica.
