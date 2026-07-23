---
Tipo: cierre-de-fase
Fase: 04
Título: Cierre de la Fase 4 — antes de seguir
---

## 🏁 Cierre de la Fase 4 — Workflows avanzados

> [!info] Para qué es esta página
> No es un ejercicio nuevo: es una **parada para consolidar**. La Fase 4 es de nivel alto (versionado, recuperación, hooks). Si algo no lo tienes claro, **para y repásalo** antes de seguir.

---

## 🎓 Lo que has aprendido en la Fase 4

- A crear **tags** y **Releases** en GitHub, con notas y descargas.
- El flujo **hotfix** de emergencia (parte de `main`, se fusiona en `main` **y** `develop`).
- El flujo completo **git-flow** (con rama `release/*`) y su comparación con GitHub Flow.
- A **recuperar** trabajo perdido con `git reflog` (incluida la notación `HEAD@{N}`).
- A crear **funciones** de terminal (en PowerShell y en Git Bash).
- A investigar con `git blame` **quién y cuándo** cambió una línea.
- A automatizar con un **hook** `commit-msg` que valida el formato.
- A limpiar la historia con **rebase interactivo** (squash/reword/drop/reorder).
- A trabajar con varias ramas a la vez con **`git worktree`**.
- **SemVer** y **CHANGELOG** para versionar y documentar cambios.

---

## ❓ Preguntas de repaso (no seguimos hasta entender esto)

> [!question] Responde en tu bitácora antes de seguir
> 1. ¿Qué diferencia hay entre un tag y una Release?
> 2. ¿De dónde parte un hotfix y en qué ramas se fusiona?
> 3. ¿Qué guarda el reflog y cómo recuperas con `HEAD@{N}`?
> 4. ¿Qué hace un rebase interactivo y cuándo NO debes usarlo?
> 5. ¿Cuándo subes MAJOR, MINOR o PATCH en SemVer?
> 6. ¿Por qué un hook `commit-msg` no llega a GitHub?

---

## ✅ Tabla de verificación (¿sé hacerlo yo solo?)

> [!success] Marca solo lo que puedas hacer SIN mirar los apuntes
> | Sé… | ¿Sí? |
> | :--- | :---: |
> | Crear un tag anotado y una Release | ☐ |
> | Hacer un hotfix y fusionarlo en `main` y `develop` | ☐ |
> | Recuperar trabajo con `git reflog` | ☐ |
> | Limpiar commits con `git rebase -i` | ☐ |
> | Aplicar SemVer a mis versiones | ☐ |
> | Mantener un CHANGELOG.md | ☐ |

---

## 🚑 Errores frecuentes de toda la Fase 4

> [!bug] Si algo falla, empieza por aquí
> | Síntoma | Causa habitual | Solución |
> | :--- | :--- | :--- |
> | El tag no aparece en GitHub | No hiciste `push --tags` | Sube los tags aparte. |
> | El bug "vuelve" tras un hotfix | No fusionaste en `develop` | Fusiona `main`→`develop` tras el hotfix. |
> | El hook no se ejecuta | Le pusiste extensión al archivo | Debe llamarse `commit-msg`, sin extensión. |
> | Rebase interactivo rompió a otros | Rebasaste algo compartido | Interactivo solo sobre historia privada. |
> | Números de versión sin sentido | No aplicas SemVer | MAJOR/MINOR/PATCH según el tipo de cambio. |

---

> [!tip] ¿Y ahora?
> Solo queda la **Fase 5 — Integración profesional** (GitHub Actions, despliegue, seguridad, proyecto final de equipo). Es la más avanzada del curso.
