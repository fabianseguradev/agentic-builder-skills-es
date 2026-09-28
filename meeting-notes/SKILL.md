---
name: meeting-notes
description: Procesa transcripciones de reuniones y las convierte en resúmenes estructurados en markdown. Usa este skill siempre que el usuario pegue la transcripción de una reunión, comparta notas de una reunión o diga algo como "procesa esta reunión", "resume esta llamada", "extrae las tareas pendientes", "aquí está la transcripción de mi llamada" o "aquí están mis notas de la reunión". Funciona con transcripciones de cualquier herramienta (Fireflies, Otter, Granola, Zoom, etc.). Actívalo incluso si el usuario solo pega un bloque de texto que parece una transcripción con los hablantes identificados.
---

# Meeting Notes Processor

Estás procesando la transcripción de una reunión (de cualquier herramienta de transcripción) para convertirla en un archivo markdown limpio y estructurado, guardado localmente.

## Qué extraer

Recorre la transcripción con atención y extrae:

1. **Metadatos de la reunión** — fecha, hora, participantes (con sus roles/cargos si se mencionan), título o tema de la reunión
2. **Resumen ejecutivo** — 3-5 oraciones que capturen el propósito central, los puntos clave de la discusión y el resultado de la reunión. Escríbelo para alguien que no estuvo en la llamada.
3. **Decisiones clave** — cosas concretas que el grupo acordó o resolvió. Distínguelas de las tareas: las decisiones son resultados, las tareas son cosas por hacer.
4. **Tareas** — cada tarea, seguimiento o compromiso mencionado. Asigna cada una a una persona específica según el contexto. Si una tarea claramente no tiene asignación, haz tu mejor suposición sobre quién sería el dueño lógico y márcala con `[SIN ASIGNAR - responsable sugerido]`.
5. **Preguntas abiertas** — cosas que se plantearon pero no se resolvieron, preguntas que necesitan respuesta o temas que se dejaron para después.
6. **Próximos pasos** — cualquier próxima reunión, fecha límite u objetivo compartido del equipo que se haya mencionado.

## Reglas para asignar tareas

- Si alguien dice "yo me encargo de X" o "¿puedes ocuparte de Y?" — asígnala directamente.
- Si nadie reclama una tarea pero hay un experto en el tema en la llamada (p. ej., la tarea es de diseño y hay un diseñador presente) — asígnasela y márcala como `[SIN ASIGNAR - sugerido: Nombre]`.
- Si es realmente ambigua y no hay ninguna deducción razonable — márcala `[SIN ASIGNAR]`.
- Nunca inventes asignaciones con seguridad — marca la incertidumbre claramente.

## Formato de salida

Guarda el archivo en `~/meeting-notes/` (crea la carpeta si no existe) usando este patrón de nombre de archivo:
`YYYY-MM-DD_[meeting-topic-slug].md`

Usa la fecha de la transcripción. Si no se encuentra ninguna fecha, usa la fecha de hoy. Convierte el tema en slug (minúsculas, guiones, sin caracteres especiales). Ejemplo: `2026-03-05_q1-product-review.md`

Usa exactamente esta estructura markdown:

```
# [Título de la reunión]
**Fecha:** [Fecha]
**Duración:** [Duración si está disponible]
**Participantes:** [Nombre (Rol), Nombre (Rol), ...]

---

## Resumen ejecutivo
[3-5 oraciones]

---

## Decisiones clave
- [Decisión 1]
- [Decisión 2]

---

## Tareas

### [Nombre de la persona]
- [ ] [Descripción de la tarea] — *para el [fecha si se mencionó]*

### [Nombre de la persona]
- [ ] [Descripción de la tarea]

### Sin asignar
- [ ] [Descripción de la tarea] — *[SIN ASIGNAR - sugerido: Nombre]*

---

## Preguntas abiertas
- [Pregunta o tema sin resolver]

---

## Próximos pasos
- [Próxima reunión, fecha límite u objetivo compartido]
```

Si una sección no tiene nada que agregar (p. ej., no hay preguntas abiertas), omítela por completo — no incluyas una sección vacía.

## Después de guardar

Dile al usuario:
- El nombre del archivo y la ruta completa donde se guardó
- Un resumen breve de una oración de la reunión (distinto del resumen ejecutivo — todavía más condensado, como un asunto de email)
- Cuántas tareas se encontraron y cuántas se marcaron como sin asignar
- Pregúntale si quiere que se amplíe o ajuste alguna sección
