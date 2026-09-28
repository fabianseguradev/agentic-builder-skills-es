# Testimonial Ask

El mensaje exacto para pedir un testimonio, más las tres preguntas que producen una cita que vale la pena usar.

Dos cosas salen mal: la mayoría nunca pide, y los que sí piden lo hacen tan vagamente que reciben "¡genial trabajar contigo!" — que es cálido, inútil y no vende nada. Este skill elige el momento correcto, escribe el pedido e incluye la **versión de redactarlo por ellos**, donde tú escribes la cita y ellos la editan, que consigue por lejos la tasa de respuesta más alta.

## Instalación

1. Copia la carpeta `testimonial-ask` en tu directorio de skills de Claude Code:
   ```bash
   cp -r testimonial-ask ~/.claude/skills/
   ```
2. Reinicia Claude Code (o empieza una nueva sesión).
3. Invócalo escribiendo `/testimonial-ask`.

## Cómo usarlo

Ejecuta `/personalize` una vez primero. Luego escribe `/testimonial-ask` y dile quién es el cliente, qué hiciste y lo último bueno que dijeron sobre ello.

Obtienes un mensaje corto listo para enviar en el hilo que ya usas con ellos, las tres preguntas que producen una cita real de antes y después, y reglas para ordenar una respuesta divagante en algo limpio sin ponerles palabras en la boca. También escribe el mensaje de permiso, porque una cita que no puedes publicar no vale nada. Todo se guarda en `~/testimonials/`.
