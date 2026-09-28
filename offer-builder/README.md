# Offer Builder

Convierte "este es mi producto" en una oferta escrita, lista para presentar, a la que es difícil decirle que no.

Esto sigue la Ecuación de Valor de Alex Hormozi. La gente compra cuando el valor se siente alto, y el valor sube cuando el resultado es más grande y más creíble, y baja cuando toma más tiempo y más esfuerzo. Así que toda la construcción se trata de **apilar un entregable contra cada obstáculo real** que tiene tu comprador, y luego quitarle el riesgo con una garantía.

## Instalación

1. Copia la carpeta `offer-builder` en tu directorio de skills de Claude Code:
   ```bash
   cp -r offer-builder ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/offer-builder`.

## Cómo usarlo

Escribe `/offer-builder`. Lee tu perfil de marca en `~/.claude/brand-profile.md`, así que ejecuta `/personalize` primero si no lo has hecho. Luego te guía por nueve pasos: nombrar el resultado soñado, enumerar lo que impide a la gente conseguirlo, apilar un entregable contra cada obstáculo, recortar el tiempo y el esfuerzo, ponerle nombre a la oferta, escribir una garantía, agregar urgencia verdadera y agregar bonos.

Obtienes la oferta terminada guardada en `~/offers/<offer-name>.md`, más una oración que puedes decir en una llamada o poner en una página de ventas.
