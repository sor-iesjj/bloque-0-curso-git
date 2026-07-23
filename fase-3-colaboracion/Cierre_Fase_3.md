---
Tipo: cierre-de-fase
Fase: 03
Título: Cierre de la Fase 3 — antes de seguir
---

## 🏁 Cierre de la Fase 3 — Colaboración con GitHub

> [!info] Para qué es esta página
> No es un ejercicio nuevo: es una **parada para consolidar**. La Fase 3 es la que de verdad convierte Git en una herramienta de **equipo** (binomios). Si algo de esto no lo tienes claro, **para y repásalo** antes de seguir.

---

## 🎓 Lo que has aprendido en la Fase 3

- A dar **acceso de colaborador** (Write) a tu compañero/a de binomio.
- El **Pull Request**: abrirlo, describirlo, **revisarlo** (Approve / Request changes / Comment) y **fusionarlo**.
- El modelo **fork + upstream**: contribuir a repos donde no eres colaborador y mantener el fork al día.
- Los **Issues** como tickets de bug/mejora, y a cerrarlos con **`Closes #N`** desde un PR.
- A **proteger `main`** para hacer obligatorio el flujo PR + revisión.
- Las tres formas de fusionar un PR: **merge commit**, **squash**, **rebase and merge**.
- Automatizaciones de equipo: **CODEOWNERS**, **Draft PR** y **plantilla de PR**.

---

## ❓ Preguntas de repaso (no seguimos hasta entender esto)

> [!question] Responde en tu bitácora antes de seguir
> 1. ¿Qué es un Pull Request y por qué no se fusiona directo a `main`?
> 2. ¿Qué diferencia hay entre trabajar como **colaborador** y desde un **fork**?
> 3. ¿Qué son `origin` y `upstream` en un fork?
> 4. ¿Cómo se cierra un Issue automáticamente desde un PR?
> 5. ¿Cuándo usas **squash** y cuándo **rebase and merge**?
> 6. Si trabajáis en binomio, ¿cómo garantizáis que todo pase por revisión?

---

## ✅ Tabla de verificación (¿sé hacerlo yo solo?)

> [!success] Marca solo lo que puedas hacer SIN mirar los apuntes
> | Sé… | ¿Sí? |
> | :--- | :---: |
> | Añadir un colaborador a mi repo | ☐ |
> | Abrir un PR con buen título y descripción | ☐ |
> | Revisar un PR y dejar comentarios en línea | ☐ |
> | Fusionar un PR (merge / squash / rebase) | ☐ |
> | Hacer un fork y sincronizarlo con el upstream | ☐ |
> | Crear un Issue y cerrarlo con `Closes #N` | ☐ |
> | Proteger la rama `main` | ☐ |

---

## 🚑 Errores frecuentes de toda la Fase 3

> [!bug] Si algo falla, empieza por aquí
> | Síntoma | Causa habitual | Solución |
> | :--- | :--- | :--- |
> | El compañero no puede hacer push | No es colaborador / no aceptó la invitación | Añádelo con permiso Write; que acepte el email. |
> | El PR compara ramas equivocadas | Base/Compare mal | Base = destino (`develop`/`main`); Compare = tu rama. |
> | El Issue no se cierra solo | Escribiste `Closes 1` sin `#` | Usa `Closes #1`. |
> | `push` directo a `main` rechazado | La protección funciona (¡bien!) | Abre un PR: es el flujo correcto. |
> | El fork da conflictos en el PR | Fork desactualizado | Sincroniza con `upstream` antes de trabajar. |

---

> [!tip] ¿Y ahora?
> Con la Fase 3 sabes colaborar en equipo de forma profesional. Las Fases 4 y 5 (workflows avanzados, integración) son **ampliación**: el profesor indicará si se hacen y para quién.
