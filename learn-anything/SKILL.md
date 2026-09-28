---
name: learn-anything
description: Te enseña un tema a tu nivel real, con práctica en lugar de una clase magistral. Averigua lo que ya sabes, te muestra la forma de la cosa antes de los detalles, te da las cinco ideas que cargan con la mayor parte, luego una escalera de tres ejercicios — 15 minutos, una hora, una noche — y termina con la idea equivocada que casi siempre cargan los principiantes en ese tema. Úsalo cuando el usuario diga "enséñame", "explícame X", "quiero aprender", "ayúdame a entender", "no entiendo cómo funciona X", "explícamelo como si tuviera cinco años", "por dónde empiezo con", "necesito aprender esto para el lunes", "dame un curso intensivo" o /learn-anything.
---

# Learn Anything — enséñame bien, en pasadas cortas

La mayoría de las explicaciones fallan de una de dos formas: están planteadas al nivel equivocado, o son un muro de texto sin nada que hacer al final. Este skill encuentra tu punto de partida real, te da la forma antes de los detalles y te entrega tres ejercicios que puedes hacer esta noche. Terminas sabiendo hacer una cosa real, no habiendo leído una página.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Encuentra su nivel real — tres preguntas, no más
Hazlas juntas en un mensaje corto:

1. **¿Qué sabes ya sobre esto?** Incluso "nada" es una respuesta útil.
2. **¿Por qué ahora?** Qué estás intentando hacer o entender — un trabajo, un proyecto, curiosidad, una conversación que quieres poder seguir.
3. **¿Qué tan profundo necesitas llegar?** Lo suficiente para mantener una conversación / lo suficiente para tomar decisiones / lo suficiente para hacerlo tú mismo.

Luego haz lo que de verdad calibra el nivel: **nombra una cosa cercana que probablemente sí conocen y compruébalo.** "Ya has usado una hoja de cálculo — ¿las fórmulas tienen sentido para ti?" Su sí o su no te dice más que la autoevaluación. La gente se subestima constantemente.

Devuélveles su nivel en una línea y empieza ahí. Nunca abras con definiciones si ya las superaron.

### 2. Da la forma antes de los detalles
Antes de cualquier dato, da un **mapa en menos de 120 palabras**: para qué sirve esta cosa, cuáles son las piezas principales y cómo se conectan. Luego una analogía honesta con algo que ya conocen según sus respuestas del paso 1.

Di en qué falla la analogía. Toda analogía tiene fugas, y decirles dónde les ahorra una creencia equivocada más adelante.

Termina esta pasada preguntando: **"¿Esa forma tiene sentido antes de que la complete?"** Detente y espera. No sigas si dicen que no — vuelve a dibujar el mapa de otra manera en lugar de explicar con más fuerza.

### 3. Enseña las cinco ideas que cargan con el 80%
Elige exactamente cinco. No siete, no doce. Las cinco que, si solo supieran esas, les permitirían seguir la mayoría de las conversaciones y tomar bien la mayoría de las decisiones de principiante.

Para cada una, en este orden:
- **La idea en una oración**, en palabras simples.
- **Por qué existe** — qué problema resuelve. La gente olvida los datos y recuerda las razones.
- **Un ejemplo concreto** con detalles reales, no un marcador de posición.

Mantén cada idea en menos de 100 palabras. Entrégalas en **dos pasadas, no en una** — las ideas 1 a 3, luego detente y haz una pregunta de comprobación. Una pregunta real con respuesta, como "si pasara X, ¿cuál de estas lo explicaría?" No "¿se entiende?". Luego las ideas 4 y 5.

Si responden mal la pregunta de comprobación, ese es el momento más útil de la sesión. Vuelve a enseñar esa idea de otra forma antes de continuar.

### 4. Construye la escalera de práctica — tres peldaños
Esta es la parte que hace que se quede. Tres ejercicios, cada uno lo bastante concreto como para empezar sin tener que hacer otra pregunta.

- **Peldaño 1 — 15 minutos.** Algo que pueden hacer ahora mismo con lo que ya tienen en su computadora o en la habitación. Con funcionamiento garantizado. El punto es el contacto con la cosa, no el desafío.
- **Peldaño 2 — una hora.** Aplican las cinco ideas a algo propio — su situación, sus datos, su proyecto. Aquí es donde deja de ser abstracto.
- **Peldaño 3 — una noche (90 minutos).** Una cosa pequeña y completa, de principio a fin, con un resultado visible que podrían mostrarle a alguien. Algo que se rompería si hubieran entendido mal.

Para cada peldaño escribe: qué hacer, cómo se ve "terminado" y el único lugar donde la gente se traba más cómo destrabarse. Si el tema se presta, el peldaño de la noche debería terminar con algo que puedan enviarle a una persona real.

### 5. Nombra la idea equivocada
Todo tema tiene una creencia equivocada que los principiantes cargan durante meses y que arruina en silencio su razonamiento. Nómbrala claramente:

> **Lo que cree la mayoría de los principiantes:** ...
> **Lo que es realmente cierto:** ...
> **Cómo notar la diferencia en la práctica:** ...

Elige la que causa más daño aguas abajo, no el error trivial más común.

### 6. Da la siguiente pregunta, no una lista de lecturas
Cierra con una pregunta que estarán listos para hacer después del peldaño 3, y una línea sobre adónde lleva. Una lista corta de dos o tres fuentes realmente buenas está bien — nunca un muro de links. Si no estás seguro de que un recurso todavía exista o siga siendo preciso, dilo en lugar de inventar uno.

## Resultado — guárdalo
Escribe en `~/learning/<topic-slug>.md` (crea `~/learning/` si hace falta) con:

```
# <Tema> — <su nivel, en tres palabras>
## La forma
## Las cinco ideas
## Escalera de práctica
### Peldaño 1 — 15 minutos
### Peldaño 2 — una hora
### Peldaño 3 — una noche
## La idea equivocada
## La siguiente pregunta
## Notas para mí
```

Deja la sección **Notas para mí** como una pregunta vacía: "¿Qué te sorprendió? ¿Qué se rompió?" Diles que agreguen una línea cada vez que vuelvan.

Dile al usuario la ruta y di: haz el peldaño 1 ahora, mientras está fresco. Son quince minutos.

## Ejemplo (entrada → salida)
**Entrada:** "No dejo de escuchar sobre DNS cuando la gente habla de sitios web y yo solo asiento. Tengo un dominio que compré y no logro apuntarlo a nada. Enséñame lo suficiente como para dejar de estar confundido."

**Salida (guardada en `~/learning/dns.md`), comprimida:**

> **Nivel:** tiene un dominio, nunca tocó un panel de configuración, necesita hacer que funcione de verdad.
>
> **La forma:** DNS es una guía telefónica. Los dominios son nombres que la gente recuerda; los servidores tienen números. DNS es la búsqueda que convierte uno en el otro. Tres piezas: el *registrador* (donde compraste el nombre), los *nameservers* (qué guía telefónica manda) y los *registros* (las entradas reales). Dónde falla la analogía: una guía telefónica es un solo libro, y DNS son miles de copias que se actualizan a distintas velocidades — por eso los cambios tardan horas en aparecer.
>
> **Las cinco ideas:** (1) Un registro A apunta un nombre a un número. (2) Un CNAME apunta un nombre a otro nombre — es lo que te dan los servicios de hosting. (3) Los nameservers deciden qué guía telefónica cuenta, y solo uno puede estar a cargo. (4) El TTL es cuánto tiempo se guarda en caché la respuesta vieja, y por eso ves el sitio viejo después de cambiarlo. (5) Nada en DNS es instantáneo, y eso no es un error.
>
> **Pregunta de comprobación después de la idea 3:** "Cambiaste el registro hace una hora y todavía ves la página vieja. ¿Cuál de las cinco lo explica?"
>
> **Escalera:** *15 min* — ejecuta `dig yourdomain.com` y lee lo que devuelve; terminado cuando puedas señalar el registro A. *1 hora* — apunta tu dominio a un hosting gratuito y mira cómo se resuelve. *Una noche* — pon un sitio de una página ahí y mándale el link a alguien.
>
> **La idea equivocada:** los principiantes creen que "no funciona" significa que lo hicieron mal. Normalmente significa que el TTL no ha vencido. Cómo saberlo: compruébalo desde tu teléfono con datos móviles — otra red, otra caché.

## Notas / casos especiales
- El error de principiante que esto evita: leer sobre un tema durante horas y no tener nada que puedan hacer. Si no hay escalera, no es enseñar.
- Nunca sueltes las cinco ideas de una vez. Dos pasadas con una pregunta de comprobación real en el medio es todo el método.
- Si responden "no sé nada" a todo, elige tú el nivel según por qué lo están aprendiendo y di qué nivel elegiste, para que puedan corregirte.
- Si el tema es enorme ("enséñame marketing"), redúcelo a una porción utilizable y di qué recortaste. Enseña bien esa porción en lugar de recorrer mal todo el campo.
- Si el tema cambia rápido o no estás seguro de que un detalle esté actualizado, márcalo claramente en lugar de adivinar — y pasa a **research-brief** para el estado actual.
- Si quieren *construir* la cosa en lugar de entenderla, enseña rápido los peldaños 1 y 2 y dedica el tiempo al peldaño 3.
