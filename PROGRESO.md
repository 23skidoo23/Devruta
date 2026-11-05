# Progreso — DevRuta

Fase actual: **1 · Fundamentos web (HTML, CSS, responsive)**
Tema actual: CSS básico para `fase-1-estatica/index.html` (hoja externa y selectores de etiqueta listos)

## Fases

- [x] Fase 0 · Git y GitHub: instalación, configuración, primer repositorio — checkpoint: repositorio `devruta` en GitHub con el primer commit
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
  - [x] Prompts específicos (archivo, restricciones, terminado comprobable) — 2026-10-31
  - [x] Referenciar archivos con `@` (sin `@` la IA puede revisar una versión vieja del archivo) — 2026-11-03
  - [x] Capturas de pantalla (el código dice que *debería* funcionar; la captura demuestra que *funciona*) — 2026-11-05
- [ ] Fase 2 · verificación con pruebas, depuración por causa raíz, IA con Git y `gh`
- [ ] Fase 3 · modo plan, `SPEC.md` por entrevista, autocompletado, checkpoints y `/rewind`, skills propias
- [ ] Fase 4 · pruebas primero (TDD), subagentes, `/code-review`, MCP, hooks, `/compact`, IA dentro de la app
- [ ] Fase 5 · Claude Code en GitHub Actions, `claude -p`, worktrees y sesiones en paralelo, permisos y sandbox, plugins

## Bitácora de sesiones

<!-- Claude agrega una entrada al final de cada sesión, la más reciente arriba -->

### Sesión 6 — 2026-11-05
- **IA:** ✅ técnica "capturas de pantalla": pegué una captura del navegador (`Win + Shift + S` → `Ctrl + V`) y la IA comprobó el resultado real contra el código.
- **CSS:** hoja de estilos externa `style.css` conectada con `<link rel="stylesheet" href="style.css">` en el `<head>` (el `href` debe coincidir con el nombre real del archivo).
  - Regla = selector + `{ propiedad: valor; }`. Selector de etiqueta: `h3 { ... }` afecta a todos los `h3`.
  - Siempre cerrar cada declaración con `;`, aunque sea la última.
  - Colores por nombre (`darkblue`) o hexadecimal (`#00008b`); `font-family` con fuentes de respaldo.
  - **Contraste:** `aquamarine` sobre gris claro casi no se leía; lo cambié a `#005C3F`. Se comprueba con el verificador de WebAIM.
- **HTML:** corregí "estará" y quité los "·" de los párrafos de las fases.
- **Git:** commit `3c31f34` subido. En `git status --short`, `M` = modificado y `??` = archivo nuevo que Git aún no sigue.
- **DevRuta:** la página ya tiene fondo, tipografía y colores en los títulos.
- Siguiente paso: seguir con CSS (modelo de caja: `margin`, `padding`, `border`) para separar y enmarcar las fases. Técnica de IA siguiente: hacer preguntas sobre el código.

### Sesión 5 — 2026-11-03 a 2026-11-05
- **IA:** ✅ técnica "referenciar archivos con `@`": la IA lee el archivo real en lugar de mi descripción. Sin `@`, puede revisar una versión vieja que quedó en su contexto.
  - Aprendo mejor con **ejemplos cortos** que luego replico (quedó guardado en la memoria de Claude).
  - **MDN** (Mozilla Developer Network / MDN Web Docs) es la documentación oficial de HTML, CSS y JS: si la IA y MDN no coinciden, gana MDN.
- **HTML:** etiquetas semánticas: `header`, `main`, `footer`, `section` (bloque temático con su `h2`) y `article` (contenido que se entiende solo, con `h3`). Enlaces con `<a href="...">texto</a>`: `href` es un atributo.
  - `ol` es para listas con orden y `ul` para listas sin orden. No repetir la misma información dos veces.
  - Replicar un ejemplo es copiar la estructura y poner mi propio contenido, no copiar el texto ("Ir a MDN").
  - Las comillas invertidas `` ` `` son de Markdown; en HTML se ven tal cual.
- **Git:** commit `c0ee9ae` subido. Un commit por tema (solo `index.html`, `PROGRESO.md` aparte). El área de preparación (*staging*) guarda una foto del archivo: si lo edito después del `add`, tengo que volver a hacer `add`. `HEAD -> main` es donde estoy y `origin/main` es lo que tiene GitHub; `17dd415..c0ee9ae main -> main` confirma el push.
- **DevRuta:** el `<body>` tiene perfil, las 6 fases del roadmap como `article` y el enlace a GitHub en el footer.
- Pendientes menores: acento en "estará" (línea 17) y el "·" suelto al inicio del párrafo de la Fase 0.
- Siguiente paso: empezar CSS (enlazar una hoja de estilos y los primeros selectores). Técnica de IA siguiente: pegar capturas de pantalla para comparar un diseño con el resultado.

### Sesión 4 — 2026-10-31
- **IA:** ✅ técnica "prompts específicos": archivo + restricciones + terminado **comprobable** (no confundir el terminado con el objetivo). Una restricción clave en esta fase: "explícame, no lo escribas".
- **HTML:** esqueleto básico (`<!DOCTYPE>`, `<html lang>`, `<head>`, `<meta charset>`, `<meta viewport>`, `<title>`, `<body>`). Lo generé con Emmet (`!` + `Tab`) y entiendo cada línea.
  - Probé quitar el viewport: con el `<body>` vacío no se nota; sin él, en el celular el contenido se vería diminuto.
  - Ver la página: doble clic al archivo (`file:///`), y luego el ciclo editar → `Ctrl + S` → `F5`.
- **Git:** commit `c82f4a2` subido. `git add <archivo>` para elegir qué entra (en vez de `add .`), `status` antes de cada commit; un `add` exitoso no imprime nada.
- **DevRuta:** se agregó `fase-1-estatica/index.html` con el esqueleto.
- Siguiente paso: técnica de IA "referenciar archivos con `@`" y llenar el `<body>` con etiquetas semánticas (perfil y lista de fases).

### Sesión 3 — 2026-10-31
- **Git:** ✅ checkpoint de la Fase 0 cerrado. Hice mi primer commit (`b420727`) y lo subí a GitHub: `git init`, `status`, `add .`, `commit -m`, `log --oneline`, `remote add origin`, `remote -v`, `push -u origin main`.
  - Comprobé que el correo del commit es el `@users.noreply.github.com`.
  - Las advertencias `LF will be replaced by CRLF` son normales en Windows (finales de línea distintos), no son errores.
  - Un `.gitignore` con `*` y `!.gitignore` ignora todo menos a sí mismo.
- **IA:** la salida real de la terminal manda; la IA también se equivoca (predijo mal que `.codegraph/` no aparecería en `git status`).
- **DevRuta:** repositorio publicado en https://github.com/23skidoo23/Devruta
- Siguiente paso: técnica de IA de la Fase 1 (prompts específicos) y empezar `fase-1-estatica/index.html`.

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

- ~~¿Cuándo conviene usar aceptar ediciones?~~ Respondida (sesión 3): cuando ya aprobé el plan y puedo revisar después con `git diff`; cobra sentido desde la Fase 3.
