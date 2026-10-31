# Progreso — DevRuta

Fase actual: **0 · Preparación con Git y GitHub**
Tema actual: cerrar el checkpoint con el primer commit (al iniciar la Fase 1)

## Fases

- [ ] Fase 0 · Git y GitHub: instalación, configuración, primer repositorio — checkpoint: repositorio `devruta` en GitHub con el primer commit
- [ ] Fase 1 · Fundamentos web (HTML, CSS, responsive) — checkpoint: página estática de DevRuta publicada
- [ ] Fase 2 · JavaScript, npm y Git en equipo — checkpoint: progreso interactivo con localStorage
- [ ] Fase 3 · React y Tailwind — checkpoint: DevRuta en React publicada
- [ ] Fase 4 · Node.js, APIs REST, PostgreSQL, JWT, Redis — checkpoint: app completa con login
- [ ] Fase 5 · Linux, AWS, CI/CD, Terraform, Ansible — checkpoint: DevRuta desplegada con CI/CD

## Avance en Git y GitHub

- [x] Fase 0 · `git config`, cuenta de GitHub con 2FA, primer repositorio
- [ ] Fase 1 · `init`, `status`, `add`, `commit`, `log`, `.gitignore`, `remote`, `push`, GitHub Pages
- [ ] Fase 2 · ramas, `merge`, conflictos, `pull`, `clone`, README, issues, pull requests
- [ ] Fase 3 · flujo con pull requests, revisión de código, `diff`, `restore`, `stash`
- [ ] Fase 4 · secretos y `.env`, `revert`, `tag` y releases
- [ ] Fase 5 · GitHub Actions, secretos del repositorio, protección de main

## Avance en programación con IA

- [x] Fase 0 · Claude Code en VS Code, ventana de contexto, `CLAUDE.md`, permisos, `/clear`, `/context`
  - [x] Asistente de código y modo agente (leer, buscar, ejecutar, editar) — 2026-10-21
  - [x] Ventana de contexto y alucinaciones — 2026-10-28
  - [x] `CLAUDE.md` como memoria y `/context` — 2026-10-29
  - [x] Modos de permisos — 2026-10-29
  - [x] Controles: `Esc` y `/clear` — 2026-10-29
- [ ] Fase 1 · prompts específicos, referencias con `@`, capturas de pantalla, preguntas sobre el código
- [ ] Fase 2 · verificación con pruebas, depuración por causa raíz, IA con Git y `gh`
- [ ] Fase 3 · modo plan, `SPEC.md` por entrevista, autocompletado, checkpoints y `/rewind`, skills propias
- [ ] Fase 4 · pruebas primero (TDD), subagentes, `/code-review`, MCP, hooks, `/compact`, IA dentro de la app
- [ ] Fase 5 · Claude Code en GitHub Actions, `claude -p`, worktrees y sesiones en paralelo, permisos y sandbox, plugins

## Bitácora de sesiones

<!-- Claude agrega una entrada al final de cada sesión, la más reciente arriba -->

### Sesión 2 — 2026-10-29
- **IA:** terminé el bloque de IA de la Fase 0.
  - `CLAUDE.md` es memoria permanente: sobrevive a `/clear` y se comprueba con `/context`. Agregué la regla de recordarme la siguiente técnica de `/ia-pro`.
  - Modos de permisos (manual, aceptar ediciones, plan, automático): practiqué cambiar de modo, aprobar y rechazar ediciones. En aceptar ediciones, los archivos se editan solos pero los comandos se preguntan. Antes de aprobar un `npm install` reviso que el paquete exista y sea el correcto.
  - `Esc` detiene una respuesta que se desvía; `/clear` va entre tareas distintas, siempre después de guardar en archivos lo importante.
- **DevRuta:** sin cambios de código.
- Siguiente paso: iniciar la Fase 1 con el primer commit (`init`, `add`, `commit`, `push`) para cerrar el checkpoint de la Fase 0, y después `fase-1-estatica/index.html`.

### Sesión 1 — 2026-10-21
- **IA:** aprendí qué es un asistente en modo agente (leer, buscar, ejecutar, editar) y por qué reviso y autorizo cada acción.
- **Git:** Git 2.50.1 instalado; configuré `user.name`, `user.email` e `init.defaultBranch main` con `--global`.
- **Seguridad:** cuenta de GitHub `23skidoo23` con 2FA; correo privado `@users.noreply.github.com` y bloqueo de pushes que expongan mi correo. Aprendí a revisar el correo de un commit con `git log` y con `.patch` en GitHub.
- **DevRuta:** repositorio vacío creado en https://github.com/23skidoo23/Devruta (sin README para no tener dos historiales).
- Siguiente paso: al iniciar la Fase 1, primer commit con `init`, `add`, `commit` y `push` para cerrar el checkpoint de la Fase 0. Seguir con `/ia-pro` (ventana de contexto y alucinaciones).

### Sesión 0 — 2026-10-17
- Se definió el proyecto DevRuta y las reglas de trabajo en CLAUDE.md.
- Se agregó Git y GitHub como parte del curso desde el día 1.
- Se agregó la ruta de programación profesional con IA (skill `ia-pro`).
- Siguiente paso: instalar Git, configurarlo y crear el repositorio `devruta` en GitHub (los comandos los escribo yo); instalar Claude Code en VS Code y comprobar con `/context` que carga este CLAUDE.md. Después, crear `fase-1-estatica/index.html`.

## Dudas pendientes

- ¿Cuándo conviene usar aceptar ediciones?
