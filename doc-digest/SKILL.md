---
name: doc-digest
description: Apúntalo a un documento largo — un contrato, un informe, un paper, un hilo de emails enorme, un muro de texto — y recibe lo que de verdad importa — las decisiones que contiene, lo que te pide, los números, las fechas, cualquier cosa que parezca una trampa y las preguntas que hay que hacer antes de firmar o responder. Separa "lo que dice" de "lo que deberías hacer al respecto" para que nunca confundas las dos cosas. Úsalo cuando el usuario diga "léeme esto", "resume este documento", "qué dice este contrato", "no tengo tiempo de leer esto", "a qué me estoy comprometiendo", "hay algo sospechoso aquí", "explícame este informe", "hazme un TLDR de esto", "qué significa esto" o /doc-digest.
---

# Doc Digest — lo que dice, y qué hacer al respecto

Los documentos largos esconden las partes importantes en el medio. Las partes que te cuestan dinero suelen ser una sola oración enterrada en la página cuatro. Este skill lee todo y extrae las decisiones, las fechas, los números, las trampas y las preguntas que deberías hacer antes de responder o firmar — con una línea firme entre lo que el documento realmente dice y lo que tú podrías hacer al respecto.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Consigue el documento
Acepta cualquiera de estos:
- Una ruta de archivo (`.txt`, `.md`, `.pdf`, `.docx`, `.csv`, `.html`). Léelo.
- Texto pegado directamente en el chat.
- Una URL, si hay acceso a la web.

Si es un PDF de más de diez páginas, léelo por partes y lleva una nota acumulada mientras avanzas para que no se te escape nada. Si de verdad no puedes abrir el archivo, dilo claramente y pídeles que peguen el texto o lo guarden como `.txt` — no adivines contenidos que no has leído.

### 2. Haz una pregunta, solo si la respuesta cambia el resultado
Pregunta como máximo una cosa: **"¿Qué vas a hacer con esto — firmarlo, responderlo, decidir algo o solo entenderlo?"**

Esa respuesta cambia lo que extraes. Firmar significa condiciones y trampas. Responder significa pedidos y plazos. Decidir significa opciones y costos de oportunidad. Si ya lo dijeron, sáltate la pregunta.

### 3. Léelo de una pasada y extrae las seis cosas
Recorre todo el documento y reúne:

1. **Qué es este documento** — una línea. Quién lo escribió, a quién va dirigido, para qué sirve.
2. **Decisiones que contiene** — cualquier cosa que ya se haya decidido, o que el documento pide que se decida. Cita la línea.
3. **Lo que te pide** — cada pedido, obligación o acción asignada al lector. Incluye las implícitas.
4. **Números y fechas** — dinero, porcentajes, cantidades, plazos, periodos de preaviso, fechas de renovación, duraciones. Cópialos exactamente. Nunca redondees, nunca estimes.
5. **Cosas que parecen trampas** — mira el paso 4.
6. **Lo que falta** — cosas que esperarías que un documento así dijera y no dice. El silencio suele ser la trampa.

Cita la línea o la página de origen de cualquier cosa importante. Si estás deduciendo en lugar de citar, márcalo `(inferido)`.

### 4. Haz el barrido de trampas
Busca específicamente estas. Es donde suele estar el daño.

- **Renovación automática** y cuánto preaviso requiere cancelar.
- **Derechos unilaterales** — cualquier cosa que una parte puede hacer y la otra no (cambiar el precio, terminar antes, cambiar las condiciones).
- **Quién es dueño de qué** al final — el trabajo, los datos, las cuentas, los archivos.
- Lenguaje de **exclusividad o no competencia**.
- **Condiciones de pago** — cuándo, cuánto retraso cuenta como tarde, qué pasa si se paga tarde, quién paga las comisiones.
- **Responsabilidad e indemnización** — quién carga con el riesgo si algo sale mal.
- **Palabras vagas haciendo mucho trabajo** — "razonable", "según sea necesario", "cada cierto tiempo", "a nuestra discreción". Significan que decide la otra parte.
- **Números que no cuadran** o que se contradicen con otros del documento.
- **Definiciones que difieren del lenguaje común** — un documento que define "Servicios" de forma estrecha en la página uno cambia cada oración posterior.

Enumera cada trampa con la línea citada y una oración simple sobre por qué importa. No dramatices. Si una cláusula es normal y está bien, di que es normal y está bien.

### 5. Separa "lo que dice" de "lo que deberías hacer"
Escríbelos como dos secciones separadas, con encabezados claros. Nunca las mezcles.

- **Lo que dice** son solo citas y hechos del documento. Sin opinión.
- **Lo que deberías hacer al respecto** es tu lectura: qué aclarar, qué objetar, qué aceptar. Cada punto aquí tiene que remitir a una línea de la sección anterior.

### 6. Escribe las preguntas que hay que hacer antes de firmar o responder
De cinco a ocho preguntas, con las palabras exactas que el usuario podría enviar. Cada una apunta a una trampa, a un hueco o a un número que no está fijado. Que se puedan responder con una oración — no reflexiones abiertas.

Luego agrega una lista breve de **Vale la pena consultar con un profesional**: cualquier cosa que involucre leyes, impuestos, empleo, inmigración, temas médicos o dinero importante. Nombra el tipo de profesional. No des asesoría legal ni financiera, no les digas si deben firmar y no digas si una cláusula es exigible o no — no te corresponde a ti decidirlo.

## Resultado — guárdalo
Escribe en `~/digests/<doc-name>-<YYYY-MM-DD>.md` (crea `~/digests/` si hace falta), con estos encabezados en orden:

```
# Resumen — <nombre del documento>
## En una línea
## Lo que dice
### Decisiones
### Lo que te pide
### Números y fechas
## Trampas y cosas a vigilar
## Lo que falta
## Lo que deberías hacer al respecto
## Preguntas antes de firmar o responder
## Vale la pena consultar con un profesional
```

Dile al usuario la ruta y dale en tu respuesta la línea más importante de todo el documento para que la vea sin abrir nada.

## Ejemplo (entrada → salida)
**Entrada:** Un contrato freelance de 14 páginas de un cliente nuevo. El usuario está por firmarlo y quiere saber a qué se está comprometiendo.

**Salida (guardada en `~/digests/client-contract-2026-07-30.md`), comprimida:**

> **En una línea:** Un acuerdo de servicios freelance de 12 meses, £2,500/mes, que se renueva solo y le entrega al cliente la propiedad de todo lo que hagas.
>
> **Números y fechas:** £2,500/mes · facturas pagadas "dentro de los 60 días de su recepción" (p. 4) · plazo inicial de 12 meses desde el 1 de septiembre · 90 días de preaviso por escrito para cancelar (p. 9).
>
> **Trampas:**
> - "El presente Acuerdo se renovará automáticamente por plazos sucesivos de 12 meses" (p. 9). Tienes que cancelar 90 días antes del 31 de agosto o quedas atado por otro año.
> - "Pago dentro de los sesenta (60) días de la recepción de la factura" (p. 4). Eso significa que tú financias dos meses de trabajo.
> - "Todo el producto del trabajo, incluidos los materiales preexistentes incorporados en él, será propiedad exclusiva del Cliente" (p. 6). Tal como está redactado, eso alcanza a tus propias plantillas que trajiste contigo.
>
> **Lo que deberías hacer al respecto:** pedir condiciones de pago a 30 días, excluir tus plantillas preexistentes de la cláusula de propiedad y poner un recordatorio en el calendario para el 1 de junio por el aviso de renovación.
>
> **Preguntas para hacer:** "¿Podemos pasar las condiciones de pago a 30 días?" · "¿Podemos agregar: los materiales preexistentes propiedad del Contratista siguen siendo propiedad del Contratista, con licencia al Cliente?" · "¿El preaviso de 90 días es negociable a 30?"
>
> **Vale la pena consultar con un profesional:** las cláusulas de propiedad e indemnización de las p. 6 y p. 11 — un abogado especialista en contratos, antes de firmar.

## Notas / casos especiales
- El error de principiante que esto evita: hojear un documento largo, no ver nada que asuste y firmar. La parte que asusta casi nunca está escrita de forma que asuste.
- Si el documento es escaso o vago, dilo — "aquí no hay mucho" es un hallazgo real. No rellenes el resumen para que parezca exhaustivo.
- Nunca inventes una cláusula, un número ni una referencia de página. Si no encuentras algo que esperarías, ponlo en **Lo que falta**, no en lo que dice.
- Nunca aconsejes sobre si firmar, si una cláusula es legal o qué haría un tribunal. Señálalo y deriva a un profesional.
- Si es un paper de investigación en lugar de un contrato, cambia el barrido de trampas por: tamaño de la muestra, qué se midió realmente, quién lo financió y si la conclusión es más amplia de lo que los datos respaldan.
- Si leerlo deja al usuario atascado entre opciones, pasa a **decision-helper**. Si necesitan responderlo, pasa a **email-writer**.
