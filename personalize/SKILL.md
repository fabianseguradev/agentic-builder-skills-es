---
name: personalize
description: Configura (o actualiza) tu perfil de marca para que todos los demás skills de este pack escriban con TU voz, para TU oferta y TU audiencia. Ejecútalo UNA VEZ antes de usar los skills de contenido, de YouTube o de dinero. Actívalo siempre que el usuario diga "personaliza", "configura mi marca", "configura mi perfil", "haz míos estos skills", "actualiza la información de mi marca", o cuando otro skill informe que el perfil de marca falta o está incompleto.
---

# Personalize — tu configuración de marca de una sola vez

Todos los skills de contenido y de dinero de este pack leen un único archivo — `~/.claude/brand-profile.md` — para poder escribir con tu voz, para tu oferta, dirigidos a tu audiencia, sin que tengas que volver a explicarte cada vez. Este skill crea o actualiza ese archivo entrevistándote. **Solo lo haces una vez** (edítalo cuando quieras ejecutando `personalize` de nuevo).

## Qué hacer

### 1. Revisa si existe un perfil
Lee `~/.claude/brand-profile.md`.
- Si existe y parece completo, muéstrale al usuario un resumen breve y pregunta si quiere actualizar alguna sección. Vuelve a preguntar solo las secciones que quiera cambiar.
- Si falta o está incompleto, haz la entrevista de abajo.

### 2. Entrevista (que sea rápida y humana)
Haz estas preguntas en grupos pequeños, **un grupo por mensaje**, no todas a la vez. Acepta respuestas cortas y deduce valores por defecto razonables; nunca sermonees. Si el usuario dice "todavía no lo sé" sobre la oferta/prueba, regístralo con honestidad (los skills luego preguntarán con más suavidad u omitirán afirmaciones) en lugar de inventar nada.

**Grupo A — Tú**
- ¿Tu nombre (cómo debería aparecer en el contenido)?
- ¿A qué te dedicas / cuál es tu área de experiencia, en una oración simple?

**Grupo B — Tu audiencia**
- ¿A quién intentas llegar (su rol/situación)?
- ¿Cuál es el principal dolor u objetivo con el que los ayudas?

**Grupo C — Tu oferta**
- ¿Qué vendes (o planeas vender), y más o menos a qué precio?
- ¿Cuál es la transformación que alguien obtiene con ello?

**Grupo D — Tu voz**
- ¿Alguna palabra/frase que te encante o que prohíbas? (p. ej., sin rayas largas, DMs en minúsculas, sin jerga)
- ¿Tu tono en tres palabras (p. ej., "directo, cálido, concreto")?

**Grupo E — Prueba y links** (opcional — sáltate lo que no tengan)
- ¿Algún resultado, credencial o logro real que te sientas cómodo citando?
- ¿Tu sitio web, tus redes sociales principales y tu link de reservas/pago?
- ¿En qué plataformas publicas más?
- ¿Tu llamado a la acción por defecto (qué quieres que haga la gente)?

### 3. Escribe el perfil
Escribe `~/.claude/brand-profile.md` usando exactamente la plantilla de `references/brand-profile-template.md` (cópiala, completa cada respuesta y deja marcadores honestos de `(aún no definido)` en los espacios vacíos). Confírmale la ruta al usuario y dile: *"Listo — todos los skills de contenido y de dinero van a usar esto automáticamente a partir de ahora. Ejecuta `personalize` cuando quieras para actualizarlo."*

## Reglas
- Nunca fabriques resultados, ingresos, cantidades de seguidores ni credenciales. Los espacios vacíos quedan vacíos hasta que el usuario te dé algo real.
- Mantén la entrevista en ~5 intercambios cortos. Respeta a un usuario que quiere responder todo en un solo mensaje.
- Este archivo es personal; vive en `~/.claude/`, nunca dentro de un proyecto o un repo.
