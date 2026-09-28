---
name: hooks
description: Genera ganchos para videos de YouTube usando el marco de Kallaway basado en deseos. Produce la Alineación de los Tres Ganchos (visual + hablado + texto), aplica los Cuatro Mandamientos, los relaciona con deseos centrales y puntúa cada gancho. Actívalo con frases como 'escribe un gancho para', 'ideas de ganchos para mi video', 'ayúdame con la intro', 'genera ganchos', 'escribe la apertura de', o cualquier pedido de ganchos, intros o líneas de apertura para videos de YouTube.
---

# YouTube Hook Generator — marco de Kallaway

Genera ganchos de YouTube de alta retención usando el sistema completo de Kallaway basado en deseos. Cada gancho se puntúa según los Cuatro Mandamientos y se entrega como una Alineación de los Tres Ganchos (visual + hablado + texto).

## Personalización
Este skill trabaja con *tu* voz de marca, para *tu* audiencia. Antes de ejecutarlo, carga el perfil de marca en `~/.claude/brand-profile.md`.
- Si no existe, ejecuta primero el skill **personalize** (o simplemente dime tu nicho, tu audiencia y tu oferta — yo lo creo).
- Usa la Audiencia y el Dolor principal del perfil para escribir ganchos con el lenguaje que tus espectadores realmente usarían consigo mismos, no texto de marketing genérico.
- Si falta un campo que este skill necesita, haré una pregunta rápida y guardaré la respuesta en el perfil.
- Nunca inventes datos ni resultados sobre el usuario — usa solo lo que está en el perfil, o pregunta.

## Cuándo se activa este skill

**Actívalo cuando el usuario quiera:**
- Escribir un gancho para un video que está planeando
- Generar líneas de apertura o guiones de intro
- Mejorar un gancho existente
- Conseguir varias opciones de gancho para probar

**Ejemplos de activación:**
- "Escribe ganchos para mi video sobre automatizar informes para clientes"
- "Ideas de ganchos para 'Cómo conseguí mis primeros 10 clientes'"
- "Ayúdame a clavar la intro de este video"
- `/hooks` o `/hooks <concepto del video>`

## Entrada

El usuario aporta uno o más de estos:
- **Concepto/tema del video** — de qué trata el video
- **Brief de la idea** — un resultado de posicionamiento o de ideación
- **Esquema** — la estructura del video
- **Puntos clave** — los datos/revelaciones más interesantes

Si el usuario solo aporta un tema, haz UNA pregunta: "¿Qué es lo más sorprendente de este video que probablemente tu audiencia no sabe?" Esa respuesta se convierte en el material central del gancho.

## El marco de Kallaway

### Fase 1 — Identifica el deseo

**Relaciónalo con uno de los Cuatro Jinetes:**
- **Dinero** — ganarlo, ahorrarlo, hacerlo crecer
- **Tiempo** — ahorrarlo, no desperdiciarlo, recuperar horas
- **Salud** — reducir el estrés, evitar el agotamiento, claridad mental
- **Estatus** — parecer inteligente, ir adelante, impresionar a los pares

**Aplica una desviación estándar:**
No apuntes al deseo central directamente — eso activa el detector de mentiras. Empaquétalo a un paso de distancia usando un deseo sustituto.

| Deseo central | Directo (detector de mentiras) | Sustituto (una desviación estándar) |
|------------|-------------------------------|-------------------------------|
| Dinero | "Gana más dinero" | "Automatiza la parte de tu trabajo que odias" |
| Tiempo | "Ahorra 10 horas a la semana" | "Nunca más empieces un proyecto desde una página en blanco" |
| Estatus | "Conviértete en experto" | "Construye lo que tus pares creen que requiere un equipo entero" |
| Salud | "Reduce el estrés laboral" | "Deja de hacer a mano lo que una herramienta resuelve en segundos" |

### Fase 2 — Genera ganchos usando cinco variaciones basadas en deseos

Genera al menos un gancho en CADA variación (llena los corchetes con el tema real del usuario):

**1. Sobre Mí (mirando hacia atrás)**
"Acabo de [lograr X] usando [Y]"

**2. Si Yo (mirando hacia adelante)**
"Si quisiera [lograr X], haría [Y]"

**3. A Ti (el espectador como personaje)**
"Si estás intentando [X], usa [Y]"

**4. ¿Se Puede? (el espectador como pregunta)**
"¿Es posible [X] en menos de [Y]?"

**5. Él/Ella Acaba de (prueba de un tercero)**
"[Z] acaba de lograr [X] en menos de [Y]"

### Fase 3 — Aplica formatos de gancho

Para los 2-3 ganchos basados en deseos más fuertes, reescríbelos con los formatos que mejor encajen:

1. **Revelación de un secreto** — insinúa ideas desconocidas o implicaciones futuras
2. **Caso de estudio** — cómo alguien logró un resultado de forma inesperada
3. **Comparación** — compara al instante dos versiones para mostrar el estado óptimo
4. **Pregunta** — implanta curiosidad directamente
5. **Educación** — presenta un proceso paso a paso
6. **Lista** — un conjunto ordenado de elementos
7. **Contrario** — una postura audaz a contracorriente
8. **Experiencia personal** — enfoque de historia en primera persona
9. **Problema** — agita un punto de dolor y luego prepara la solución

Elige los 2-3 formatos que encajen con el contenido. No fuerces los nueve.

### Fase 4 — Puntúa con las seis palabras de poder del gancho

Para cada gancho, comprueba que contenga:

1. **Sujeto** — de quién trata el video (yo, nosotros, tú, [la persona])
2. **Acción** — el verbo (construí, automaticé, reemplacé, descubrí)
3. **Objetivo** — el resultado final
4. **Contraste** — compara estados (antes vs. después, de 0 a X, manual vs. automatizado)
5. **Prueba** (opcional) — respalda la perspectiva ("otra vez", "después de probar 50 herramientas")
6. **Tiempo** (opcional) — agrega urgencia ("en un fin de semana", "en menos de 5 minutos")

### Fase 5 — Alineación de los Tres Ganchos

Para los 3 mejores ganchos, genera la alineación completa:

**Gancho visual** — ¿Qué se muestra en pantalla en los primeros 1-3 segundos?
- Activa el "procesamiento de abajo hacia arriba" (respuesta visual subconsciente ~200ms)
- Colores, movimiento, imágenes inesperadas

**Gancho hablado** — ¿Qué se dice en los primeros 5-15 segundos?
- La línea del gancho, escrita con un nivel de lectura de quinto grado
- 1-3 oraciones como máximo
- Debe abrir un bucle de curiosidad que el video cierra

**Gancho de texto** — ¿Qué texto aparece en pantalla?
- El título o una versión acortada
- Complementa (no duplica) el gancho hablado
- Crea una brecha de curiosidad JUNTO CON el gancho hablado

**Los tres tienen que apuntar a la misma idea al mismo tiempo.**

### Fase 6 — Lista de los Cuatro Mandamientos

Puntúa cada gancho principal (pasa/no pasa):

1. **Alineación** — ¿Coinciden los ganchos visual, hablado y de texto? ✓/✗
2. **Velocidad al valor** — ¿Cero demora, cero relleno antes de que el gancho pegue? ✓/✗
3. **Claridad** — ¿El espectador sabe exactamente de qué trata el video en una oración? ✓/✗
4. **Curiosidad** — ¿Abre una pregunta en la mente del espectador? ✓/✗

Tiene que pasar LOS CUATRO para recomendarlo. Si uno falla, anota cómo arreglarlo.

## Formato de salida

```
## Mapa del deseo
- **Deseo central:** [Jinete]
- **Deseo sustituto:** [Una desviación estándar]

## Mejores ganchos

### Gancho 1 — [Formato] + [Variación]
**Hablado:** "[La línea del gancho]"
**Visual:** [Qué hay en pantalla]
**Texto en pantalla:** "[El texto]"
**Palabras de poder:** Sujeto ✓ Acción ✓ Objetivo ✓ Contraste ✓ Tiempo ✓ (5/6)
**Mandamientos:** Alineación ✓ Velocidad ✓ Claridad ✓ Curiosidad ✓ (4/4)

### Gancho 2 — ...
### Gancho 3 — ...

## Las cinco variaciones (como referencia)
1. Sobre Mí: "..."
2. Si Yo: "..."
3. A Ti: "..."
4. ¿Se Puede?: "..."
5. Él/Ella Acaba de: "..."

## Recomendación
[Qué gancho usar y por qué — directo y con opinión]
```

## Principios clave

- **El gancho son los 15 segundos más importantes.** Más tiempo aquí que en 5 minutos de contenido del cuerpo.
- **Nivel de lectura de quinto grado.** Oraciones cortas. Palabras comunes. El lenguaje complejo mata los ganchos.
- **Curiosidad sin clickbait.** El gancho tiene que prometer algo que el video cumple. Una audiencia se va para siempre ante una promesa exagerada.
- **Los ganchos contrarios necesitan autoridad.** "X está mal" solo funciona con credibilidad inmediata (investigación, datos, prueba personal).
- **El enfoque negativo atrae más.** "Estás desperdiciando 5 horas a la semana" rinde más que "Ahorra 5 horas a la semana". La aversión a la pérdida es real.
- **Un gancho por video.** No metas varios ángulos en la apertura. Elige uno. Comprométete.
