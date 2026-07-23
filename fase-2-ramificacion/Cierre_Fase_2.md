---
Tipo: cierre-de-fase
Fase: 02
Título: Cierre de la Fase 2 — antes de seguir
---

## 🏁 Cierre de la Fase 2 — Ramificación y estrategias de merge

> [!info] Para qué es esta página
> No es un ejercicio nuevo: es una **parada para consolidar**. La Fase 2 es la más importante para trabajar en **binomio** (dos alumnos compartiendo un repositorio). Si esto no lo tienes claro, **para y repásalo** antes de seguir.

---

## 🎓 Lo que has aprendido en la Fase 2

- Qué es una **rama** y cómo trabajar en paralelo sin romper `main` (`git switch -c`).
- A **fusionar** ramas (`git merge`) y qué es un **fast-forward**.
- El flujo profesional de **dos ramas permanentes**: `develop` (taller) y `main` (escaparate).
- El patrón **feature branch**: una rama por trabajo, que se fusiona en `develop`.
- Cómo se hace una **release** (`develop → main`) y se etiqueta con un **tag** (`v1.0.0`, SemVer).
- A **resolver conflictos** de merge (leer las marcas `<<<`, `===`, `>>>`).
- A **aparcar** trabajo a medias con `git stash`.
- Herramientas de nivel: **rebase** (histórico lineal), **cherry-pick** (un commit suelto), **revert** (deshacer sin borrar), **bisect** (encontrar el commit que rompió algo).

---

## ❓ Preguntas de repaso (no seguimos hasta entender esto)

> [!question] Responde en tu bitácora antes de seguir
> 1. ¿Para qué sirve una rama y por qué protege a `main`?
> 2. ¿Qué papel tienen `develop` y `main`, y de cuál nacen las features?
> 3. ¿Por qué se produce un **conflicto** de merge y cómo se resuelve?
> 4. ¿Cuál es la **regla de oro** del rebase?
> 5. En una rama **compartida**, ¿por qué se usa `revert` y no `reset --hard`?
> 6. Si dos personas (un binomio) trabajan el mismo repo, ¿cómo evitan pisarse el trabajo?

---

## ✅ Tabla de verificación (¿sé hacerlo yo solo?)

> [!success] Marca solo lo que puedas hacer SIN mirar los apuntes
> | Sé… | ¿Sí? |
> | :--- | :---: |
> | Crear una rama y cambiarme a ella | ☐ |
> | Fusionar una rama con `git merge` | ☐ |
> | Trabajar con el flujo `feature → develop → main` | ☐ |
> | Hacer una release con tag (`v1.0.0`) | ☐ |
> | Resolver un conflicto de merge a mano | ☐ |
> | Aparcar y recuperar trabajo con `git stash` | ☐ |
> | Deshacer un commit compartido con `git revert` | ☐ |

---

## 🚑 Errores frecuentes de toda la Fase 2

> [!bug] Si algo falla, empieza por aquí
> | Síntoma | Causa habitual | Solución |
> | :--- | :--- | :--- |
> | Editaste en la rama equivocada | No miraste `git branch` | Comprueba la rama antes de editar; mueve el trabajo si hace falta. |
> | Merge detenido: "CONFLICT" | Dos ramas tocan la misma línea | Resuelve las marcas y `git add` + commit; o `git merge --abort`. |
> | Rebase te rompió commits de otros | Rebasaste una rama compartida | No rebases lo compartido; usa merge. |
> | Rompiste el repo del compañero | `reset --hard` + `--force` | En lo compartido usa `git revert`. |
> | Ramas viejas acumuladas | No borraste las features fusionadas | `git branch -d` (local) y `git push origin --delete` (remota). |

---

> [!tip] ¿Y ahora?
> Con la Fase 2 dominas lo necesario para trabajar en **binomio** compartiendo un repositorio. Las Fases 3, 4 y 5 (colaboración avanzada, workflows, integración) son **ampliación**: el profesor indicará si se hacen y para quién.
