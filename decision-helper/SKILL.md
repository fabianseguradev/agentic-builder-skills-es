---
name: decision-helper
description: Estás atascado entre opciones y dando vueltas en círculos. Esto fuerza una decisión, no otro resumen — pone las opciones reales sobre la mesa, nombra qué estás optimizando de verdad, saca a la luz la restricción que no has dicho en voz alta y te da una recomendación clara con la razón en una sola línea, más el primer paso para hoy. Úsalo cuando el usuario diga "ayúdame a decidir", "estoy atascado entre", "no puedo elegir", "debería hacer X o Y", "no dejo de ir y venir", "qué harías tú", "llevo semanas pensando en esto", "ayúdame a pensar esta decisión", "pros y contras" o /decision-helper.
---

# Decision Helper — elige una, muévete hoy

Estar atascado rara vez es falta de información. Normalmente es una restricción sin nombre, o dos cosas que quieres y que no pueden ganar ambas. Este skill saca las opciones reales, nombra el intercambio que de verdad estás haciendo y termina con una recomendación y un primer paso. No un resumen equilibrado — una decisión.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Pon las opciones sobre la mesa — las reales
Pídele al usuario que plantee la decisión en una oración y luego que enumere todas las opciones que está considerando.

Después haz las dos cosas que no harán por sí mismos:
- **Agrega las opciones que faltan.** Casi toda decisión atascada se plantea como dos opciones cuando hay cuatro. Las que suelen faltar: no hacer nada por ahora, hacer una versión más pequeña de una opción, hacer ambas en secuencia, pedirle a alguien algo que cambie la decisión por completo.
- **Quita las opciones falsas.** Cualquier cosa que ya descartaron pero siguen enumerando para sentirse exhaustivos. Dilo claramente: "No vas a hacer esta — la quito."

Termina con una lista numerada limpia de las opciones vivas. Normalmente de dos a cuatro.

### 2. Nombra qué estás optimizando de verdad
Pregunta: **"Si solo una de estas cosas pudiera ser cierta dentro de un año, ¿cuál sería?"** Dales la lista para elegir — dinero, tiempo, riesgo, aprendizaje, libertad, reputación, conservar la relación, quitárselo de encima, proteger tu energía.

Haz que elijan **una**. Dos está bien si de verdad están empatadas, pero no más. Si se niegan a elegir, esa negativa es el problema real y deberías decirlo.

Luego devuélveselo en una línea: "Entonces estás optimizando X, y estás dispuesto a renunciar a Y para conseguirlo." Observa si se incomodan. Si se incomodan, elegiste la equivocada.

### 3. Saca a la luz la restricción que no han dicho en voz alta
Este es el paso importante. La gente se queda atascada porque la razón real da vergüenza, o porque no se la han admitido a sí mismos. Indaga con delicadeza con las que apliquen:

- ¿Hay una cifra de dinero que por sí sola decide esto? ¿Cuál es la cantidad mínima que lo haría obvio?
- ¿Hay una persona cuya reacción estás gestionando — una pareja, un jefe, un padre o una madre, un amigo?
- ¿Hay una fecha desde la que no estás contando? ¿Un contrato de alquiler que termina, un contrato, una fecha de entrega, el margen de tus ahorros?
- ¿Alguna de estas opciones en realidad trata de demostrarle algo a alguien?
- ¿Seguirías atascado si nadie se enterara nunca de cuál elegiste?
- ¿Qué es lo que te daría alivio si la decisión se tomara por ti mañana?

La última pregunta es la más fuerte. El alivio apunta a la respuesta. Cuando algo salga a la luz, escríbelo en una oración simple — normalmente esa es toda la decisión.

### 4. Haz la prueba de reversibilidad
Pregunta: **si esto resulta estar mal, ¿qué tan difícil es deshacerlo?**

- **Fácil de deshacer** (podrías revertirlo en una semana por menos de unos cientos y nadie sale lastimado): decide ahora, en el momento. Dilo directamente: "Esto es barato de revertir. Ya pasaste más tiempo decidiendo de lo que costaría arreglarlo. Elige y avanza." No hagas un análisis profundo de una decisión reversible.
- **Difícil de deshacer** (dinero que no puedes recuperar, un contrato, una jugada pública, una relación, una casa, dejar algo): ve más despacio por exactamente **una razón específica** — nombra la única cosa que cambiaría la respuesta y la única verificación que la resolvería. Una verificación, con fecha. No "investigar más".

Nunca dejes que una decisión difícil de deshacer se diluya en "pensarlo más". Dale una verificación y una fecha límite.

### 5. Toma la decisión
Da una recomendación. No una inclinación, no un "depende", no una tabla.

Dale exactamente este formato:

> **Haz esto:** <la opción, en palabras simples>
> **Porque:** <una línea — la única razón por la que le gana a las demás, ligada a lo que dijeron que están optimizando>
> **Estás renunciando a:** <el costo real, dicho con honestidad>
> **Estarías equivocado si:** <la única condición que daría vuelta esto>

Esa última línea importa. Les dice a qué estar atentos, y te mantiene honesto — si no puedes nombrar la condición, no tienes una recomendación, tienes una preferencia.

### 6. Nombra el primer paso, hoy
Una acción, que se pueda hacer hoy, en menos de 30 minutos. Un mensaje enviado, un número consultado, una llamada agendada, un formulario empezado, una línea escrita. No "empezar a planificar".

Luego da la **fecha límite para decidir** de lo que siga abierto, y una línea sobre qué sabrán para entonces que no saben ahora.

## Resultado — guárdalo
Escribe en `~/decisions/<short-slug>-<YYYY-MM-DD>.md` (crea `~/decisions/` si hace falta) con estas secciones:

```
# Decisión — <una línea>
## Opciones sobre la mesa
## Lo que estoy optimizando
## La restricción que no había dicho en voz alta
## Reversibilidad
## La decisión
## Primer paso (hoy)
## Fecha límite para decidir
```

Dile al usuario la ruta. Luego di el primer paso en voz alta en tu respuesta, para que puedan hacerlo sin abrir el archivo.

## Ejemplo (entrada → salida)
**Entrada:** "Llevo seis semanas yendo y viniendo sobre si dejar mi trabajo para dedicarme de lleno a mi proyecto paralelo. Gano unas £900 al mes con él. No puedo decidir."

**Salida (guardada en `~/decisions/quit-job-2026-07-30.md`), comprimida:**

> **Opciones:** (1) Renunciar ahora. (2) Quedarte y seguir construyendo de noche. (3) Bajar a cuatro días y comprarte un día de construcción a la semana. (4) Fijar una cifra de ingresos que active la renuncia.
> *Enumeraste dos. Las opciones 3 y 4 son las que no habías puesto sobre la mesa.*
>
> **Optimizando:** riesgo — específicamente no quedarte sin dinero. Renunciarás a velocidad para conseguirlo.
>
> **La restricción que no habías dicho:** tu pareja no ha aceptado esto. Cada versión del plan que describiste da por hecha una conversación que no ha ocurrido.
>
> **Reversibilidad:** difícil de deshacer. Renunciar y volver a conseguir un trabajo con el mismo salario no es trabajo de una semana. Entonces: una verificación, no cinco — ¿las £900/mes crecen cuando agregas diez horas a la semana, o están estancadas por algo que no es el tiempo?
>
> **La decisión:**
> - **Haz esto:** pide trabajar cuatro días a la semana, a partir del mes que viene.
> - **Porque:** te da lo único que no tienes — una prueba real de si más horas mueven la cifra — sin apostar el alquiler en ello.
> - **Estás renunciando a:** el 20% de tu salario, y a la historia limpia de "me lancé con todo".
> - **Estarías equivocado si:** tu empleador dice que no a los cuatro días, en cuyo caso la decisión pasa a ser renunciar o quedarte y necesitarás el disparador de ingresos en su lugar.
>
> **Primer paso hoy:** mándale un mensaje a tu pareja — "¿podemos hablar el jueves sobre la idea de pasar a cuatro días?" Doce palabras. Ese es el bloqueo, no la hoja de cálculo.
>
> **Decidir antes de:** 30 de septiembre.

## Notas / casos especiales
- El error de principiante que esto evita: investigar durante seis semanas una decisión reversible. Si es barata de deshacer, la respuesta es "elige una ahora" — dilo y dilo en serio.
- Si la entrada es escasa ("¿debería hacer esto?"), consigue las opciones y lo que se optimiza antes que nada. No puedes recomendar sin saber cómo se ve ganar para ellos.
- Nunca te cubras en el paso 5. Si de verdad no puedes decidir, di que las dos opciones son equivalentes y diles que elijan la que les daría alivio — pero dilo como la recomendación, no como un encogimiento de hombros.
- Si la decisión depende de dinero, salud, leyes o inmigración, igual toma la decisión en las partes que puedas y señala la pieza específica que vale la pena llevar a un profesional.
- Si la elección depende de datos que nadie en la conversación tiene, pasa a **research-brief** para esa pregunta específica y luego vuelve a decidir.
- Si depende de un documento que no han leído bien, ejecuta primero **doc-digest** sobre él.
