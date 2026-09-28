---
name: plan-first
description: Convierte una idea grande y difusa en un plan escrito y pequeño que apruebas antes de que Claude toque un solo archivo, para que lances una v1 en lugar de estancarte en la versión cinco. Fuerza un recorte de alcance firme, una lista de "no va en la v1", el orden de los pasos y una definición de terminado en lenguaje simple — guardado como un archivo de plan que puedes volver a abrir cualquier noche. Úsalo cuando el usuario diga "quiero construir X", "ayúdame a planificar esto", "tengo una idea", "planifica esto primero", "reduce el alcance de esto", "esto se está volviendo demasiado grande", "cómo divido esto", "primero el plan" o escriba /plan-first. Si todavía no han elegido ningún proyecto, eso es **claude-orientation**, no este skill.
---

# Plan First — decide qué vas a construir antes de construir nada

Lo número uno que mata un proyecto de principiante no es un bug. Es construir demasiado grande. Describes el sueño completo, Claude empieza a construir el sueño completo y, cuatro noches después, tienes la mitad de todo y nada funciona. Este skill toma el sueño, lo recorta a una v1 que puedes terminar en unas pocas sesiones y deja el plan por escrito para que lo apruebes antes de tocar cualquier archivo.

En este skill no se construye nada. El resultado es un plan que aceptaste, con un primer paso lo bastante pequeño como para empezar esta noche.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Saca la idea, completa
Deja que divaguen. Pregunta: "¿Qué estás intentando construir, y para quién es?" No corrijas ni achiques nada todavía — necesitas el panorama completo antes de poder recortarlo.

Luego devuélveselo en tres líneas: qué es, para quién es, qué hace. Haz que confirmen que lo entendiste antes de seguir. La mitad de los malos proyectos son un malentendido que nunca se detectó en los primeros cinco minutos.

### 2. Encuentra el único trabajo
Pregunta: "Si esto hiciera UNA sola cosa, y la hiciera bien, ¿cuál sería?"

Insiste hasta tener una sola oración con un solo verbo. "Permite que un visitante agende una llamada conmigo." "Muestra mis cinco mejores fotos y mi email." "Me dice qué comer esta semana."

Esta oración es la columna vertebral. Cada pregunta posterior se resuelve preguntando si sirve a esta oración. Escríbela palabra por palabra.

### 3. Recorta fuerte — la lista de la v1 y la lista de más adelante
Este es todo el punto del skill, así que hazlo en voz alta y sin suavidad.

Toma todo lo que describieron y clasifícalo en dos listas:

- **v1** — solo lo que el único trabajo necesita para funcionar para una persona real. Apunta a entre tres y cinco elementos. Si son más de cinco, recorta otra vez.
- **Más adelante** — todo lo demás. Logins, cuentas, pagos, paneles, paneles de administración, segundas páginas, listas de email, modo oscuro, animaciones.

Para cada cosa que recortas, di por qué en una frase: "Fuera las cuentas — nadie puede iniciar sesión en algo que todavía no funciona."

Luego dales la tranquilidad que hace que el recorte se mantenga: nada de la lista de más adelante se pierde. Está por escrito. Pueden agregarlo en la segunda semana, una vez que la cosa exista y alguien la haya usado de verdad.

Si se resisten a un recorte, haz una pregunta: "¿El único trabajo funciona sin esto?" Si la respuesta es sí, va a Más adelante.

### 4. Ordena los pasos
Convierte la v1 en entre tres y seis pasos, en orden, cada uno lo bastante pequeño como para terminarlo en una sentada de 90 minutos.

Reglas para el orden:
- El primer paso tiene que producir algo que puedan mirar. No configuración, no estructura — algo visible en pantalla.
- Cada paso se construye sobre el anterior, para que nada quede a medio terminar.
- Nombra cada paso como un resultado, no como una tarea: "la página muestra mi oferta y un botón" le gana a "construir el diseño".

### 5. Escribe cómo se ve "terminado"
Pregunta: "¿Cómo vas a saber que la v1 está terminada?" Luego convierte la respuesta en una lista comprobable de tres a cinco líneas que una persona normal podría ir marcando mirando la pantalla.

Bien: "Un desconocido en un teléfono puede leer lo que hago y tocar un botón para escribirme."
Mal: "Funciona bien."

Si no pueden saber si está terminado mirándolo, no es una definición de terminado — reescríbela hasta que lo sea.

### 6. Señala el modo plan
Diles qué hábito está entrenando este skill. Antes de cualquier sesión de construcción real, pueden poner a Claude en modo plan — Claude piensa el cambio y muestra el plan sin tocar archivos, y ellos lo aprueban antes de que pase nada. La misma idea que este skill, al nivel de una sola sesión.

Dilo claramente: leer un plan durante dos minutos es más barato que deshacer una hora de construcción equivocada.

Recuérdales también que en realidad no pueden romper nada. `/rewind` deshace los cambios. "Guarda esto como punto de control" hace un guardado permanente al que siempre pueden volver.

## Resultado — guárdalo
Escribe el plan en `~/plans/<project-slug>-plan.md` (crea `~/plans/` si hace falta), con esta forma:

```markdown
# <Proyecto> — plan de la v1
Escrito: <fecha>

## El único trabajo
<Una sola oración.>

## En la v1
- <elemento>
- <elemento>
- <elemento>

## NO va en la v1 (lista de más adelante)
- <elemento> — <una frase sobre por qué espera>
- <elemento> — <una frase sobre por qué espera>

## Los pasos, en orden
1. <paso con forma de resultado>
2. <paso con forma de resultado>
3. <paso con forma de resultado>

## Listo cuando
- [ ] <línea comprobable>
- [ ] <línea comprobable>
- [ ] <línea comprobable>

## Primer paso — empieza aquí
<Una oración. Lo exacto que hay que hacer en la próxima sesión.>
```

Diles la ruta y da una siguiente acción: "Abre una sesión nueva, lee el primer paso y haz solo eso."

## Ejemplo (entrada → salida)
**Entrada:** "Quiero construir un sitio para lo de mis comidas preparadas. La gente elige sus comidas, paga, recibe un plan semanal por email, quiero un login para que puedan ver sus pedidos anteriores y quizás un blog de recetas."

**Salida (guardada en `~/plans/meal-prep-plan.md`):**
```markdown
# Sitio de comidas preparadas — plan de la v1
Escrito: 2026-07-30

## El único trabajo
Una persona de la zona lee lo que ofrezco y me escribe para pedir una semana de comidas.

## En la v1
- Una página que dice qué son las comidas y para quién son
- Las tres opciones de comida de esta semana con una foto y un precio
- Un botón que abre un mensaje para mí
- Funciona en un teléfono

## NO va en la v1 (lista de más adelante)
- Logins y pedidos anteriores — nadie puede iniciar sesión en algo donde todavía nadie ha comprado
- Pago en línea — toma los primeros cinco pedidos por mensaje y cobra como ya cobras
- Blog de recetas — es un segundo proyecto disfrazado de este
- Emails semanales automáticos — escribe los primeros cuatro a mano y mira si alguien los lee

## Los pasos, en orden
1. La página existe y dice la oferta con claridad, de arriba a abajo
2. Las tres comidas aparecen con fotos y precios
3. El botón de mensaje funciona desde un teléfono
4. Un amigo la abre en su teléfono y puede decirme qué vendo en una oración

## Listo cuando
- [ ] Puedo abrir el link en mi teléfono y leerlo todo sin hacer zoom con los dedos
- [ ] Un desconocido puede decirme qué vendo después de diez segundos
- [ ] Tocar el botón abre un mensaje para mí con algo ya escrito
- [ ] El link está en línea y se lo mandé a una persona real

## Primer paso — empieza aquí
Construye una página que diga qué son las comidas, para quién son y nada más. Todavía sin fotos.
```

## Notas / casos especiales
- Si se resisten a cada recorte, pregunta cuál es la fecha límite. Una fecha real hace el recorte por ti.
- Si la idea en realidad son dos proyectos, dilo y haz que elijan uno. No planifiques ambos.
- Una entrada escasa ("quiero un sitio web") significa que preguntas para qué es y quién lo ve. Nunca planifiques un sitio sin un visitante en mente.
- Si ya empezaron a construir y es un desastre, este skill igual funciona — planifica la v1 desde donde están y trata el desastre como la lista de más adelante.
- Cuando el plan está aprobado y están listos para construir, salen de este skill. Vuelve al final de la sesión con **session-wrapup** para que mañana empiece en cinco minutos en lugar de treinta.
- Revisa el plan cada vez que la construcción deje de tener sentido. Un plan que nunca vuelves a abrir es un plan que no necesitabas.
