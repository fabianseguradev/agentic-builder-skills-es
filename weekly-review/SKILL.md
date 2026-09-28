---
name: weekly-review
description: Un reinicio dominical de 20 minutos que mira qué lanzaste de verdad esta semana, por qué se estancó lo que se estancó, y elige LA ÚNICA cosa para la próxima semana — luego te hace decir qué estás dejando de lado. Escribe un archivo de revisión con tus logros, tu única cosa y tres movimientos específicos programados en las horas que realmente tienes. Úsalo cuando el usuario diga "revisión semanal", "revisa mi semana", "qué logré hacer esta semana", "planifica mi semana", "reinicio del domingo", "siento que no hice nada esta semana", "en qué debería enfocarme la próxima semana", "reinicio para la semana" o escriba /weekly-review.
---

# Weekly Review — una hora de domingo que hace que la próxima semana cuente

El progreso de cada noche es invisible. Construyes 90 minutos a la vez, algunas noches no llegan a nada, y para el domingo se siente como si no hubieras hecho nada. Esa sensación está equivocada la mayoría de las veces, y es la razón principal por la que la gente abandona en el segundo mes. El progreso es semanal, no nocturno.

Esto son 20 minutos un domingo. Miras qué lanzaste de verdad, nombras por qué se estancó lo que se estancó, eliges UNA cosa para la próxima semana y recortas todo lo demás. El recorte es el punto. Cinco prioridades son cero prioridades.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Trae la evidencia real, no dependas de la memoria
La gente subestima mucho su propia semana. Ve a buscar los hechos antes de preguntarles nada.

- Lee `~/build-log.md` si existe y saca cada entrada de los últimos siete días.
- Revisa `~/plans/` por cualquier archivo de plan y anota qué había en la v1.
- Si nombran una carpeta de proyecto, revisa qué cambió esta semana (`git log --since="7 days ago" --oneline` si es un repo de git).

Luego devuélveselo como una lista: "Esto es lo que de verdad hiciste esta semana." Si el registro está vacío, pasa a preguntarles directamente — pero diles claramente que la próxima semana deberían ejecutar **session-wrapup** al final de cada sesión para que este paso tenga con qué trabajar.

### 2. Nombra los logros — incluidos los pequeños
Enumera qué se lanzó o avanzó. Sé generoso pero honesto. Un logro cuenta si:
- Algo existe ahora que no existía el lunes, o
- Algo se puso frente a una persona real, o
- Se tomó una decisión que estaba bloqueando todo lo demás.

Aprender algo no cuenta como logro por sí solo. Tampoco mirar, leer o planificar. Dilo con suavidad pero dilo — es la diferencia entre un constructor y un estudiante.

Si algo real salió en línea o se le mandó a un humano, señálalo en su propia línea. Esa es la repetición que importa.

### 3. Nombra qué se estancó, y por qué — específicamente
Para cada cosa que no avanzó, consigue la razón real. Insiste más allá de "no tuve tiempo" — todos dicen que no tuvieron tiempo. Pregunta cuál de estas fue realmente:

- **Demasiado grande** — nunca empezó porque no cabía en un bloque de 90 minutos
- **Poco claro** — no sabían cuál era el siguiente paso, así que no hicieron nada
- **Atascado** — chocaron contra una pared y dieron vueltas en círculos (eso es **stuck-unstick**)
- **Evitado** — sabían qué hacer y no quisieron hacerlo. Normalmente el que involucra a otras personas: enviarlo, publicarlo, pedir dinero.
- **De verdad sin tiempo** — pasó una semana real de la vida

La razón determina el arreglo, así que no aceptes una vaga. Escribe la razón junto a cada elemento estancado.

### 4. Elige LA ÚNICA cosa
Pregunta: "Si la próxima semana solo produjera un resultado, ¿cuál haría que la semana valiera la pena?"

Reglas:
- Una. No un top tres. Si dan tres, pregunta cuál conservarían si perdieran las otras dos.
- Tiene que poder terminarse en una semana de horas robadas.
- Debería terminar con algo que existe o algo que otra persona ve. No "trabajar en el sitio" — "el sitio está en línea y tres personas tienen el link."

Escríbela como un resultado, no como una actividad.

### 5. Fuerza el recorte
Este es el paso que hace real la revisión. Pregunta directamente: "¿Qué vas a dejar de lado esta semana?"

Haz que nombren al menos dos cosas — proyectos reales, ideas o misiones secundarias que no van a recibir atención los próximos siete días. Escríbelas bajo un encabezado llamado "No esta semana." Nada se cancela, se estaciona, y estacionar cosas es lo que hace posible la única cosa.

Si se niegan a dejar algo de lado, señala la lista de estancados del paso 3 y di la parte callada: esa lista es lo que pasa cuando nada se deja de lado.

### 6. Programa tres movimientos específicos
Pregunta qué noches realmente tienen esta semana, y cuánto tiempo. Luego coloca tres movimientos en esos espacios. Cada movimiento:

- Cabe en una sola sentada
- Se describe como un resultado ("la sección de precios está escrita y en la página"), no como una tarea ("trabajar en los precios")
- Sirve a la única cosa

Tres movimientos, no siete. Si se pierde una noche, tres igual te llevan ahí. Siete garantizan el fracaso y la culpa que viene con él.

### 7. Di la oración honesta
Termina con una línea simple sobre la semana: qué patrón notaste. "Lanzas rápido cuando el movimiento está escrito la noche anterior, y te estancas en cualquier cosa que implique enviárselo a alguien." Dilo una vez, no des una clase, y ponlo en el archivo. A lo largo de algunas semanas, estas líneas se convierten en la parte más útil del documento.

## Resultado — guárdalo
Escribe en `~/weekly-review.md`, agregando una nueva sección con fecha arriba (deja las semanas anteriores debajo — el historial es el punto). Crea el archivo si no existe.

```markdown
# Revisión semanal

## Semana del <YYYY-MM-DD>

**Lanzado esta semana**
- <logro>
- <logro>

**Estancado, y por qué**
- <cosa> — <razón específica>

**LA ÚNICA cosa de la próxima semana**
<Un resultado, en una oración.>

**No esta semana (estacionado)**
- <cosa>
- <cosa>

**Tres movimientos**
1. <noche> — <resultado>
2. <noche> — <resultado>
3. <noche> — <resultado>

**Patrón que noté**
<Una línea honesta.>
```

Diles la ruta, y da una siguiente acción: "Pon esos tres movimientos en tu calendario ahora, esta noche, mientras todavía estás aquí sentado."

## Ejemplo (entrada → salida)
**Entrada:** El usuario construyó durante cuatro noches, dejó casi terminada una landing page, nunca se la mandó a nadie, y también empezó un newsletter y una segunda idea de proyecto.

**Salida (guardada en `~/weekly-review.md`):**
```markdown
# Revisión semanal

## Semana del 2026-07-27

**Lanzado esta semana**
- La página de paseo de perros existe: titular, tres servicios con precios, botón de contacto.
- Fuentes y colores decididos y fijados, así que esa discusión terminó.
- Escribiste el texto de precios que llevaba dos semanas atascado.

**Estancado, y por qué**
- Mandarle la página a alguien — evitado. Tienes un link funcionando desde el miércoles y no lo has enviado.
- El newsletter — demasiado grande. No hay un primer número escrito ni una lista a la que mandarlo.
- La segunda idea de proyecto — poco clara. Es una oración, no un plan.

**LA ÚNICA cosa de la próxima semana**
La página está en línea en un link real y cinco personas reales la abrieron.

**No esta semana (estacionado)**
- El newsletter
- La segunda idea de proyecto

**Tres movimientos**
1. Martes — la página está en línea en una URL que le puedes mandar a alguien
2. Jueves — le mandaste el link a cinco personas y les hiciste una pregunta: "¿qué debería vender?"
3. Sábado — la página está arreglada según lo que dijeron esas cinco personas

**Patrón que noté**
Construyes rápido y te detienes en el momento en que el siguiente paso implica que otro humano lo vea. Construir no es el cuello de botella. Enviar sí lo es.
```

## Notas / casos especiales
- Si la semana de verdad no produjo nada, no fabriques logros. Dilo claramente y haz que la única cosa de la próxima semana sea muy pequeña — un resultado visible en una sola sentada. Una cosita terminada reconstruye el impulso más rápido que un discurso de ánimo.
- Si enumeran cinco prioridades, sigue preguntando "cuál conservarías" hasta que quede una. No cedas en esto.
- Nunca inventes números o resultados que no te dijeron. Lee el registro, pregunta si está escaso.
- Si lo mismo se estanca tres semanas seguidas por la misma razón, ese es el proyecto real. Dilo.
- Si la mayoría de los elementos se estancan porque son demasiado grandes, la próxima semana empieza con **plan-first**, no con construir.
- Si el registro de construcción está vacío cada semana, el arreglo está más arriba: haz que ejecuten **session-wrapup** cada noche para que esta revisión pueda hacer su trabajo.
