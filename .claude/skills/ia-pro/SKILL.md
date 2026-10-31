---
name: ia-pro
description: Ruta para aprender a programar con IA como los desarrolladores profesionales actuales (Claude Code, prompts, verificación, modo plan, subagentes, hooks, MCP, CI). Úsala cuando pida aprender o practicar una técnica de programación con IA.
argument-hint: "[técnica opcional]"
---

# Programar con IA como profesional

Técnica pedida: $ARGUMENTS
Si no pidió ninguna, lee PROGRESO.md, identifica la fase actual y enseña la siguiente técnica sin marcar de esa fase en "Avance en programación con IA".

## Cómo enseñar cada técnica
1. Qué es y qué problema resuelve, en 2 o 3 frases.
2. Un ejemplo de prompt "antes" (vago) y "después" (profesional).
3. Un ejercicio corto aplicado a DevRuta, respetando quién escribe el código según la fase en CLAUDE.md.
4. Al terminar, una pregunta para comprobar que entendió y marcar la técnica en PROGRESO.md si la domina.
No enseñes técnicas de fases futuras.

## Ruta por fase

### Fase 0 · Bases
- Qué es un asistente de código con IA y el modo agente: lee archivos, ejecuta comandos, edita.
- Ventana de contexto: todo lo que lee ocupa espacio y la calidad baja si se llena. Alucinaciones: puede inventar funciones o paquetes.
- Claude Code en VS Code. `CLAUDE.md` como memoria del proyecto y `/context` para revisar qué cargó.
- Modos de permisos (manual, aceptar ediciones, plan, automático) y por qué empezar revisando cada acción.
- Controles: `Esc` para detener, `/clear` entre tareas distintas.

### Fase 1 · Comunicar bien
- Prompts específicos: qué archivo, qué restricción, cómo se ve "terminado".
- Referenciar archivos con `@` en lugar de describirlos.
- Pegar capturas de pantalla para comparar un diseño con el resultado.
- Hacer preguntas sobre el código como a un senior ("¿por qué este elemento no se centra?").
- Verificar contra la documentación oficial (MDN).

### Fase 2 · Verificar y depurar
- Darle a la IA una forma de comprobar su trabajo: pruebas, salida esperada, capturas.
- Depurar pegando el error completo y pidiendo la causa raíz, no un parche.
- Pedir evidencia (la prueba que pasó, el comando y su salida) en lugar de aceptar "ya quedó".
- IA con Git: mensajes de commit, descripción de pull requests, la herramienta `gh`.
- Si una corrección falla dos veces: `/clear` y un prompt mejor.

### Fase 3 · Planear y construir con la IA
- Explorar → planear → programar → commit, con el modo plan (`Shift+Tab`).
- Entrevista y especificación: "entrevístame sobre esta funcionalidad y escribe SPEC.md"; luego implementar en una sesión nueva.
- Autocompletado en el editor: aceptar solo lo que entiende.
- Checkpoints y `/rewind` para probar ideas sin miedo (no sustituyen a Git).
- Skills propias: convertir los comandos de `.claude/commands/` en skills dentro de `.claude/skills/`.
- Sesiones con nombre (`/rename`) y `claude --continue` para retomar.

### Fase 4 · Calidad, seguridad y herramientas
- Desarrollo guiado por pruebas con IA: escribir pruebas primero y que la IA implemente hasta pasarlas.
- Subagentes en `.claude/agents/`: crear un `revisor-seguridad` para inyección SQL, XSS, secretos y autenticación.
- Revisión adversarial: `/code-review` o el patrón escritor/revisor en otra sesión con contexto limpio.
- MCP (`claude mcp add`) para conectar la IA a la base de datos o a GitHub.
- Hooks en `.claude/settings.json`: correr pruebas o lint después de cada edición (reglas que se cumplen siempre).
- Manejo del contexto con `/compact` y subagentes para investigar sin llenar la conversación.
- IA dentro de la app: agregar a DevRuta una función que genere quizzes llamando a una API de IA, con la llave en `.env`.
- Riesgos: secretos en prompts, paquetes inventados o maliciosos, código inseguro que parece correcto.

### Fase 5 · Automatizar y escalar
- Modo no interactivo `claude -p` en scripts.
- Claude Code en GitHub Actions para revisar pull requests automáticamente.
- Worktrees y sesiones en paralelo para trabajar en varias tareas.
- Permisos, listas de comandos permitidos, sandbox y modo automático para trabajar con seguridad.
- Plugins: instalar y evaluar plugins de la comunidad.
- Revisar con IA la infraestructura (Terraform) antes de aplicarla, leyendo siempre el plan.

Referencia: https://code.claude.com/docs/en/best-practices
