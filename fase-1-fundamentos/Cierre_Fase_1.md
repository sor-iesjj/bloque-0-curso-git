---
Tipo: cierre-de-fase
Fase: 01
Título: Cierre de la Fase 1 — antes de pasar a la ramificación
---

## 🏁 Cierre de la Fase 1 — Fundamentos de Git

> [!info] Para qué es esta página
> No es un ejercicio nuevo: es una **parada para consolidar**. Antes de pasar a la Fase 2 (ramificación), asegúrate de que de verdad has entendido lo de aquí. Si algo de esto no lo tienes claro, **para y repásalo** (o pregúntame): la Fase 2 da por sabido todo lo siguiente.

---

## 🎓 Lo que has aprendido en la Fase 1

- **Qué es Git** y en qué se diferencia de una nube o una copia de seguridad.
- A **instalar** Git y a moverte por la terminal (PowerShell o Git Bash).
- A **identificarte** ante Git (`user.name`, `user.email`).
- La **estructura de trabajo**: una bóveda contenedor (sin versionar) con repositorios dentro (`Manuales/`, `Bitacora/`).
- El **ciclo básico**: `git init` → editar → `git add` → `git commit` → `git push`.
- A **ver el estado** (`git status`), **las diferencias** (`git diff`) y el **historial** (`git log`).
- A **deshacer** antes del commit (`git restore`) y a **enmendar** el último commit (`--amend`).
- A **proteger secretos** con `.gitignore`.
- A **traer cambios** del remoto (`git pull`) y a **clonar** repos ajenos (`git clone`).
- Las **dos vías de autenticación** (SSH y HTTPS + token).
- Extras de técnico: **alias**, **mantenimiento** (`fsck`/`gc`) y **firma** de commits.

---

## ❓ Preguntas de repaso (no pasamos hasta entender esto)

> [!question] Responde en tu bitácora antes de seguir
> 1. Explica las **tres zonas** de Git y qué comando mueve un archivo entre ellas.
> 2. ¿Por qué **nunca** se hace `git init` sobre la bóveda contenedor?
> 3. ¿Qué diferencia hay entre `git add` y `git commit`?
> 4. ¿Cuál es la **regla de oro** al trabajar en el centro y en casa?
> 5. ¿Qué NUNCA debe subirse a GitHub, y con qué se evita?
> 6. Nombra las dos formas de autenticarse con GitHub y una diferencia entre ellas.

---

## ✅ Tabla de verificación (¿sé hacerlo yo solo?)

> [!success] Marca solo lo que puedas hacer SIN mirar los apuntes
> | Sé… | ¿Sí? |
> | :--- | :---: |
> | Comprobar mi versión de Git | ☐ |
> | Configurar mi nombre y correo | ☐ |
> | Crear la bóveda y hacer `git init` en la carpeta correcta | ☐ |
> | Hacer el ciclo `add → commit` y leer `git status` | ☐ |
> | Publicar un repo en GitHub (por SSH o por token) | ☐ |
> | Ver diferencias con `git diff` y el historial con `git log` | ☐ |
> | Deshacer un cambio con `git restore` | ☐ |
> | Crear un `.gitignore` que proteja secretos | ☐ |
> | Bajar cambios con `git pull` y clonar con `git clone` | ☐ |

---

## 🚑 Errores frecuentes de toda la Fase 1

> [!bug] Si algo falla, empieza por aquí
> | Síntoma | Causa habitual | Solución |
> | :--- | :--- | :--- |
> | "git no se reconoce como comando" | Terminal mal / Git no instalado | Reabre la terminal; usa Git Bash en Windows. |
> | "nothing to commit" | Olvidaste `git add` | Haz `git status`; si no hay verde, falta el `add`. |
> | `push` rechazado | El remoto tiene cambios que no tienes | `git pull` y vuelve a `push`. |
> | `Permission denied (publickey)` | Clave SSH no lista | Repasa tu clave, o usa HTTPS + token. |
> | Un secreto acabó en GitHub | Faltó el `.gitignore` a tiempo | Créalo antes de trabajar; usa `git rm --cached` si ya se subió. |
> | Hiciste `git init` en la bóveda | Carpeta equivocada | Borra ese `.git/` y hazlo dentro de la carpeta de trabajo. |

---

> [!tip] Siguiente paso
> Cuando tengas la tabla de verificación completa, pasa a la **Fase 2 — Ramificación**: Marko aprende a trabajar en paralelo con ramas, a fusionarlas y a resolver sus primeros conflictos. Es la base para trabajar en **binomio** compartiendo un repositorio.
