---
name: deploy-it
description: Pon lo que acabas de construir en una dirección web pública real, gratis, un clic a la vez, y guarda el link para ir armando una lista de las cosas que has lanzado. Cubre el paso de GitHub en lenguaje simple y resuelve las tres cosas que de verdad se rompen para los principiantes. Úsalo cuando el usuario diga "/deploy-it", "pon esto en línea", "cómo subo esto a internet", "despliega mi sitio", "publica mi página", "necesito un link que pueda mandarle a alguien", "pon esto en vivo", "aloja mi sitio web gratis", "saca esto de mi computadora", "cómo comparto lo que construí" o "mi sitio está en línea pero la página sale en blanco".
---

# Deploy It — de un archivo en tu laptop a un link que puedes mandar por mensaje

Ahora mismo, lo que construiste solo existe en tu computadora. Nadie puede verlo, lo que significa que todavía no cuenta. Esto lo pone en una dirección web real, gratis, en unos diez minutos, sin que tengas que entender nada de servidores. Luego le mandas ese link a una persona hoy.

## Configuración
Ninguna. Este skill funciona tal cual.

## Pasos

### 1. Encuentra qué vamos a lanzar y fija las expectativas
Busca en `~/sites/` y `~/games/` carpetas que tengan un `index.html`. Si hay más de una, enuméralas y pregunta cuál. Si no hay ninguna, pregunta dónde está el archivo.

Luego di esto claramente:
- Esto es gratis. Sin tarjeta, sin prueba, nada que cancelar.
- Vas a hacer clic en dos sitios web y responder algunas preguntas. No vas a escribir código.
- **Feo pero en línea le gana a bonito pero local.** Hoy no lo vamos a mejorar. Lo vamos a hacer real.
- Si algo se ve aterrador, detente y dime qué ves en pantalla. No puedes romper nada.

### 2. Conviértelo en un repo de Git, en lenguaje simple
Explica el paso de GitHub antes de hacerlo, porque "repositorio" es la palabra que asusta a la gente:

> Git es un sistema de guardado que conserva cada versión de tu archivo. GitHub es un sitio web que guarda esas versiones en línea. Vercel — el hosting gratuito — lee desde GitHub y convierte tu archivo en una página web real. Esa es toda la cadena. Estás haciendo una copia guardada en línea y luego apuntando un hosting gratuito hacia ella.

Luego ejecútalo por ellos desde dentro de la carpeta de su proyecto:

```bash
cd ~/sites/<slug>
git init
git add .
git commit -m "First version"
```

Si Git pide un nombre y un email la primera vez, diles que es algo de una sola vez y configúralo:

```bash
git config --global user.name "Their Name"
git config --global user.email "their@email.com"
```

Ahora súbelo a GitHub. Si tienen la CLI de GitHub, un solo comando lo hace todo:

```bash
gh repo create <slug> --public --source=. --push
```

Si ese comando no se encuentra, guíalos por el navegador en su lugar, un paso a la vez — nunca más de una instrucción por mensaje:
1. Ve a github.com e inicia sesión (crea una cuenta gratis si hace falta — email, nombre de usuario, contraseña, eso es todo).
2. Haz clic en el **+** de arriba a la derecha y luego en **New repository**.
3. Ponle de nombre `<slug>`. No toques nada más. Haz clic en **Create repository**.
4. GitHub muestra un cuadro con comandos. Diles: "No copies nada — yo me encargo. Solo pégame la URL que aparece arriba en esa página."
5. Toma su URL y ejecuta tú mismo la conexión y el push.

### 3. Guíalos por el registro en Vercel, un clic a la vez
Vercel es el hosting gratuito. Da estos pasos uno a la vez y espera a que digan "listo" antes del siguiente:

1. Ve a **vercel.com** y haz clic en **Sign Up**.
2. Elige **Continue with GitHub**. Usa GitHub — hace que el resto sea automático.
3. Aprueba la pantalla de permisos. Vercel pide leer tus repositorios para poder publicarlos. Di que sí.
4. Elige el plan **Hobby** cuando te lo pregunte. Es el gratuito. Te pedirá tu nombre; no te pedirá una tarjeta.
5. En tu panel, haz clic en **Add New** y luego en **Project**.
6. Busca `<slug>` en la lista y haz clic en **Import**.
7. No cambies ninguna configuración. Haz clic en **Deploy**.
8. Espera unos 30 segundos. Vas a ver confeti y un link que termina en `.vercel.app`.

Pídeles que te peguen ese link.

### 4. Resuelve las tres cosas que de verdad salen mal
Revisa esto antes de celebrar, porque son las tres que hacen tropezar a casi todos los principiantes:

**1. La página sale en blanco, o muestra una lista de archivos.**
Casi siempre el archivo no se llama `index.html`, o está metido dentro de una carpeta extra. Compruébalo con:
```bash
ls ~/sites/<slug>
```
Si se llama `site.html` o `Untitled.html`, renómbralo a `index.html`. Si está una carpeta más adentro, súbelo. Luego haz commit y push de nuevo — Vercel vuelve a publicar automáticamente en segundos.

**2. El repo no aparece en la lista de importación de Vercel.**
O se creó como privado con acceso limitado, o Vercel no recibió permiso para ese repo. En la pantalla de importación hay un link **Adjust GitHub App Permissions** — haz clic y concede acceso a todos los repositorios. Actualiza la página.

**3. Hicieron push a GitHub y el sitio en línea no cambió.**
Dos causas habituales. O el cambio nunca se guardó con commit — ejecuta `git status` y, si lista archivos en rojo, todavía no se guardaron. O su navegador está mostrando la página vieja en caché — diles que abran el link en una ventana privada para comprobarlo de verdad.

Si se topan con algo que no está en esta lista, pídeles una oración que describa exactamente lo que ven en pantalla. No les pidas que lean logs.

### 5. Ábrelo en tu teléfono y luego mándaselo a un ser humano
Dos cosas, en este orden, ambas hoy:

1. **Abre el link en tu teléfono.** No en la laptop. Aquí es donde encuentras los problemas reales — texto demasiado pequeño, un botón que se sale del borde, una imagen que empuja el diseño hacia un lado. Anota lo que está mal y arréglalo en una sesión posterior. No empieces a arreglarlo ahora.
2. **Mándale el link a una persona real.** Un amigo, tu pareja, alguien de un chat grupal. No para pedir opiniones, no para recibir elogios. La repetición que cuenta es enviarlo. Algo que hiciste ahora existe en una dirección que cualquier persona del mundo puede abrir, y lo hiciste en una noche.

Si más adelante quieren una dirección más bonita, menciona que un dominio propio cuesta unos $12 al año y que Vercel te guía en el proceso — pero no hoy.

### 6. Guarda el link en tu lista
Agrega al final de `~/my-links.md` (créalo si no existe). Mantén una línea por cada cosa lanzada, la más reciente al final:

```markdown
# Cosas que he lanzado

- 2026-07-30 — Treat Chase (juego) — https://treat-chase.vercel.app — local: ~/games/treat-chase
```

Diles la ruta y por qué existe: dentro de tres meses este archivo es la respuesta a "¿qué has construido de verdad?", y esa lista vale más que cualquier certificado.

## Resultado — guárdalo
- `~/my-links.md` — una lista acumulada de cada cosa en línea que han lanzado: fecha, nombre, URL en vivo y la carpeta local.
- La carpeta del proyecto ahora es un repo de Git conectado a GitHub que se publica automáticamente en Vercel con cada push.

Indica la URL en vivo y la ruta de `~/my-links.md`. Única siguiente acción: abrirlo en su teléfono y luego mandarle el link a una persona hoy.

## Ejemplo (entrada → salida)
**Entrada:** "Hice ese juego de la serpiente con mi perro. ¿Cómo lo pongo en línea para que mi hermana pueda jugarlo?"

**Salida:**

En línea en **https://treat-chase.vercel.app** en unos 9 minutos. Un tropiezo en el camino: el primer despliegue mostró una página en blanco porque el archivo se llamaba `game.html` — lo renombré a `index.html`, hice push y volvió en 20 segundos.

Agregado a `~/my-links.md`:
```markdown
- 2026-07-30 — Treat Chase (juego) — https://treat-chase.vercel.app — local: ~/games/treat-chase
```

Siguiente: ábrelo en tu teléfono y luego mándale el link a tu hermana y pregúntale su puntaje.

## Notas / casos especiales
- El error que esto evita: construir algo bueno y nunca mostrárselo a nadie, así que nunca se vuelve real y el impulso se muere.
- Da una instrucción por mensaje durante el registro. Una lista numerada de ocho pasos pegada de una vez es donde los principiantes se pierden y abandonan.
- Nunca les pidas que lean un log de errores o un stack trace. Pregúntales qué ven en la pantalla, en una oración, y tradúcelo tú.
- Si no tienen cuenta de GitHub, es un registro de dos minutos, no un bloqueo. Díselo antes de que supongan que es algo complicado.
- Cada cambio futuro es: dime qué arreglar, luego `git add . && git commit -m "..." && git push` y el link en vivo se actualiza solo. Dilo una vez para que sepan que se vuelve más fácil.
- Derivación: **first-website**, **landing-page**, **link-in-bio**, **sales-page** o **simple-game** si todavía no hay nada construido para desplegar.
