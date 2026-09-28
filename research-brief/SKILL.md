---
name: research-brief
description: Convierte "necesito entender X antes del lunes" en un brief de una página que de verdad puedes usar. La respuesta al frente en tres líneas, luego lo que es cierto, lo que se discute, en lo que nadie se pone de acuerdo, los números con sus fechas y qué leer si quieres más. Todo tiene fuente, y cualquier cosa que no se pudo comprobar se marca como no verificada en lugar de adivinarse. Úsalo cuando el usuario diga "investiga esto por mí", "qué necesito saber sobre", "ponme al día sobre", "tengo una reunión sobre X", "ponme al corriente de", "es bueno X", "de qué va esto", "investiga esto", "necesito sonar como que sé de esto para el lunes" o /research-brief.
---

# Research Brief — una página, con fuentes, para el lunes

Necesitas entrar a algo sabiendo lo suficiente. No una lista de lecturas, no veinte pestañas — una página que diga qué es cierto, qué se discute y qué dicen realmente los números. Este skill va y lo busca, marca de dónde salió cada afirmación y se niega a llenar huecos con suposiciones seguras.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Fija la pregunta
Toma lo que te dieron y devuélveles la pregunta en una oración, más afilada de lo que la dijeron. Luego pregunta **una** cosa: **"¿Qué vas a hacer con esto?"** — una reunión, una decisión, una compra, un texto, una entrevista.

Eso cambia el brief por completo. Un brief para una compra necesita precios y modos de fallo. Un brief para una reunión necesita los dos argumentos y quién los sostiene. Di qué forma vas a escribir antes de empezar.

Si la pregunta es demasiado amplia para responderla en una página ("cuéntame sobre la IA"), redúcela a una versión respondible y di claramente a qué la redujiste.

### 2. Ve y mira
Usa la búsqueda web si está disponible. Si no lo está, dilo en una línea al principio del brief y trabaja con lo que sabes — pero marca cada afirmación que no puedas respaldar con fuente como `[no verificado]` y no finjas lo contrario.

Busca de forma deliberada, no una sola vez:
- La pregunta simple, tal como la escribiría una persona.
- La pregunta más "crítica" o "problemas" — el caso más fuerte en contra es la parte que más briefs se saltan.
- El número más específico de la pregunta, más un año.
- La fuente primaria, no el artículo sobre ella. Si existe un informe, una presentación, un paper o una página oficial, ve a eso. Los resúmenes de resúmenes se van desviando.

Apunta a entre cinco y diez fuentes de al menos tres dueños distintos. Tres artículos que citan todos el mismo comunicado de prensa son una sola fuente con tres sombreros — dilo si es lo que encuentras.

### 3. Clasifica lo que encontraste en tres pilas
Esta es la estructura que hace útil un brief, y es el paso que la gente se salta.

- **Establecido** — varias fuentes independientes coinciden, y hay una fuente primaria detrás. Dilo claramente.
- **Discutido** — gente creíble no está de acuerdo. Da ambos lados en una línea cada uno, y di quién sostiene cada posición y cuál es su interés. Nunca promedies dos posiciones en un punto medio falso.
- **Desconocido** — nadie tiene buenos datos, o los datos son demasiado nuevos para confiar en ellos. Decir "todavía nadie sabe esto" es un hallazgo genuino y a menudo la línea más útil de la página.

Si todo cae en "establecido", probablemente buscaste demasiado angosto. Vuelve y busca la crítica.

### 4. Maneja los números con cuidado
Cada número recibe tres cosas: **la cifra, la fecha de la que es y de dónde salió.** Un número sin fecha no es información.

- Copia las cifras exactamente. Nunca las redondees para que se vean más prolijas.
- Si dos fuentes dan números distintos, muestra ambos y di por qué difieren (años distintos, definiciones distintas, métodos distintos).
- Si un número tiene más de unos 18 meses en un área que cambia rápido, márcalo `[puede estar desactualizado]`.
- Si no puedes encontrar un número que el usuario claramente necesita, escribe `[no encontrado]`. Nunca estimes uno y nunca dejes pasar una cifra plausible sin fuente.

### 5. Escribe la respuesta al frente
Lo primero en la página son **tres líneas que responden la pregunta.** Alguien que lea solo esas tres líneas debería poder mantener una conversación razonable.

Luego el resto del brief las respalda. No construyas hacia la conclusión — empieza con ella.

### 6. Agrega el "para leer más" y los huecos honestos
De dos a cuatro fuentes con una línea cada una sobre por qué vale la pena el tiempo y más o menos cuánto toma. La mejor primero. Nunca un muro de links.

Luego una sección corta de **Lo que no pude verificar.** Enumera todo lo que buscaste y no pudiste confirmar, todo lo que se apoyaba en una sola fuente y todo lo que las fuentes contradicen abiertamente. Esta sección es lo que hace confiable el resto del brief — un brief sin sección de huecos es un brief que los está escondiendo.

## Resultado — guárdalo
Escribe en `~/research/<topic-slug>-<YYYY-MM-DD>.md` (crea `~/research/` si hace falta):

```
# <Pregunta> — brief
*Escrito el <fecha>. Para: <para qué lo van a usar>.*

## La respuesta (3 líneas)
## Lo que es realmente cierto
## Lo que se discute
## Lo que nadie sabe todavía
## Los números
## Si quieres más
## Lo que no pude verificar
## Fuentes
```

En **Fuentes**, enumera cada fuente con su título, quién la publica y la fecha. Dile al usuario la ruta, y pega la respuesta de tres líneas en tu respuesta para que capten el punto sin abrir el archivo.

## Ejemplo (entrada → salida)
**Entrada:** "Tengo una llamada el lunes con alguien que nos vende una prueba de semana de cuatro días. No sé nada. Ponme al día."

**Salida (guardada en `~/research/four-day-week-2026-07-30.md`), comprimida:**

> **La respuesta:** La mayoría de las pruebas publicadas de la semana de cuatro días reportan que la productividad se mantuvo estable y la rotación de personal bajó. La evidencia más fuerte viene de empresas autoseleccionadas que se ofrecieron como voluntarias, que es la razón principal por la que los críticos no aceptan los resultados. La pregunta abierta no es si funciona en una prueba — es si se sostiene después de dos o tres años, y casi nadie tiene datos tan largos.
>
> **Lo que es realmente cierto:** Varios pilotos con múltiples empresas se han ejecutado desde 2022, y la mayoría de las empresas participantes eligieron continuar después. Los días de baja por enfermedad reportados bajaron en los pilotos que los midieron.
>
> **Lo que se discute:** Si las ganancias vienen de la semana más corta o de la limpieza de reuniones y procesos que las empresas hacen para prepararse para ella. Los defensores dicen que es la semana; los escépticos dicen que se podría conseguir la mayor parte sin cortar un día. Ambos lados están leyendo los mismos pilotos.
>
> **Lo que nadie sabe todavía:** Cómo se sostiene en trabajo por turnos, hostelería y salud, donde el resultado está ligado a las horas presenciales. Los pilotos se inclinan fuertemente hacia trabajo de oficina y software.
>
> **Los números:** Las tasas reportadas de "continuaríamos" de las empresas piloto han sido altas en varias pruebas publicadas — trata cualquier porcentaje único que te citen en la llamada como venido de un piloto específico, y pregunta cuál. `[las cifras varían según el piloto; pregunta por la fuente de cualquier número que te den]`
>
> **Lo que no pude verificar:** Cifras de largo plazo más allá de tres años — no pude encontrar un estudio publicado que siga a las empresas tanto tiempo. Cualquier cosa que te digan el lunes sobre efectos de largo plazo probablemente es una extrapolación.
>
> **Pregunta en la llamada:** de qué piloto vienen sus números, cuál fue la muestra y si algo de eso cubre un negocio con la forma del tuyo.

## Notas / casos especiales
- El error de principiante que esto evita: leer cinco artículos que citan todos el mismo comunicado de prensa y terminar sintiéndose informado. Cuenta las fuentes por quién las publica, no por cuántas pestañas están abiertas.
- Nunca llenes un hueco con un número que suene plausible. `[no encontrado]` y `[no verificado]` son respuestas correctas. Que te agarren con una cifra inventada en una reunión es peor que decir que no lo sabes.
- Si la búsqueda web no está disponible, dilo en la primera línea del brief y marca todo el documento en consecuencia. No escribas en silencio de memoria como si lo hubieras comprobado.
- Si todas las fuentes son de gente que vende la cosa, dilo claramente — ese es el hallazgo.
- Temas que cambian rápido: pon la fecha al principio del brief y anota que se va a desactualizar. Un brief sin fecha es una trampa para quien lo lea dentro de seis meses.
- Si el brief existe para zanjar una elección, pasa a **decision-helper**. Si necesitan entender de verdad la mecánica en lugar del panorama, pasa a **learn-anything**.
