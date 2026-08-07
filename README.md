# Curso de Git y GitHub — 2.º SMR (práctica independiente)

> **Módulo:** SOR — Sistemas Operativos en Red · **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
> **Autor y propietario:** © 2026 Pedro Navarro Miralles. **Licencia:** [CC BY-NC-SA 4.0](LICENSE) — atribución obligatoria, uso no comercial.

## Qué es este curso (y qué NO es)

Es un **curso de Git autocontenido**, en forma de **simulación**: sigues a **Marko**, un técnico junior ficticio, y aprendes Git **desde cero**. Sirve para **entender la filosofía de trabajo** que usaremos todo el año (documentar en Obsidian, versionar con Git, sincronizar con GitHub).

> [!important] Es INDEPENDIENTE de tu trabajo real
> Este curso vive en **la bóveda de Marko**, separada de tu **bóveda SOR** real (la de la Fase 0 / prerequisitos, con la que trabajas de verdad todo el año). Aquí **no se da nada por hecho**: se instala, se configura y se crea todo otra vez, en el mundo de Marko. La forma de trabajar es **la misma** que en tu bóveda real, pero **no se mezclan**.

---

## El escenario y los personajes

- **Marko** — 19 años, recién titulado en SMR. Acaba de entrar como técnico junior en **Boochan Networks S.L.** Le toca documentar su trabajo desde cero: la empresa nunca tuvo manuales escritos.
- **Boochan Networks S.L.** — PYME ficticia de 12 empleados que da soporte de infraestructura a otras empresas. Tiene un servidor (Ubuntu Server con Active Directory, VPN, almacenamiento…).
- **Carlos** — técnico *senior*. Lo sabe todo, pero **nunca ha documentado nada** (y a veces edita los mismos archivos sin avisar).
- **Lucía** — **responsable de IT**. Es quien pide a Marko que documente todo con Git+GitHub y quien revisa su trabajo.

Cada ejercicio cuenta una situación real de Marko en la empresa.

---

## La bóveda de Marko (estructura del curso)

Marko organiza su trabajo con el **mismo patrón** que usarás tú en real, pero en su propia bóveda:

```
Boveda_Marko/                    ← se abre en Obsidian. NUNCA se hace git init aquí.
├── Bitacora/                    ← su diario de trabajo (repositorio propio)
│   └── Bloque_1_Fundamentos_Git/
└── Manuales/                    ← los procedimientos que documenta (repositorio propio)
```

> [!danger] La regla de oro (igual que en tu trabajo real)
> `Boveda_Marko/` es solo el contenedor: **no se versiona**. Lo que son repositorios son las **carpetas de dentro** (`Bitacora/`, `Manuales/`), cada una independiente. Nunca `git init` sobre la bóveda entera, o tendrías "git dentro de git".

---

## Autenticación con GitHub: dos caminos

Aprenderás **las dos formas** de conectar con GitHub. Un repositorio tiene **una identidad** pero **dos direcciones** que llevan al mismo sitio, así que puedes usar la que prefieras:

- 🔑 **SSH** *(recomendada)* — `git@github.com:usuario/repo.git`. Se configura una vez con una clave, no caduca y no pide contraseña.
- 🔐 **HTTPS + token** — `https://github.com/usuario/repo.git`. Usa un *Personal Access Token*; más sencillo de entender, pero el token puede caducar.

En cada ejercicio de conexión verás **las dos opciones** en bloques separados.

---

## Terminal: dos sintaxis

Los comandos `git` son iguales en todas partes. Cuando cambie algo (crear carpetas/archivos, rutas), verás dos bloques:

- 🐧 **Git Bash / Linux** — comandos tipo Unix (`touch`, `~/…`). Git Bash viene con Git para Windows.
- 🪟 **PowerShell** — comandos nativos de Windows (`New-Item`, `$env:USERPROFILE`).

> [!tip] Los `.md` también se crean desde Obsidian
> Crear archivos por terminal es parte del aprendizaje, pero recuerda: los ficheros `.md` (notas, manuales) también puedes crearlos **directamente en Obsidian** (clic derecho → *New note*). Usa lo que te resulte más cómodo.

---

## 📹 Grabación y entrega (LÉEME — aplica a TODAS las prácticas)

Igual que en la Fase 0, **cada práctica se graba entera con OBS**, de principio a fin. No es un repaso al final: se ve **cómo la haces tú**. Cada ejercicio trae su propia caja **📹 Grabación** y un **Paso 0** para prepararte y arrancar la grabación.

> [!important] Las 5 reglas de grabación
> 1. **Grabación completa con OBS**, sin cortes, hablando lo que haces.
> 2. **Preséntate al empezar** y **muestra tu identidad** en pantalla (Teams, correo `@alu.edu.gva.es` o, cuando lo tengas, tu perfil de GitHub). Di qué vas a hacer.
> 3. **Timestamps SIEMPRE** en la descripción: `00:00 Presentación` y **uno por cada paso** (`mm:ss`).
> 4. **Nombre del vídeo:** `B0.G.f.n.e · <título>` — donde `f.n.e` = **fase . nivel . ejercicio**. Ejemplo: `B0.G.1.1.1 · Marko instala Git`.
> 5. **Súbelo a tu playlist del curso** como **"No listado"**.

> [!info] 🎬 UNA sola playlist para todo el curso
> Se llama **`B0_Curso_Git`** — igual que tu carpeta de apuntes y que la carpeta del material. La creas una vez, al principio, y ahí van **todos** los vídeos del curso.
>
> **No hagas una playlist por fase.** El vídeo ya lleva la fase en su nombre (`B0.G.1.2.1`), así que dentro de la playlist salen ordenados solos.

> [!warning] Entrega ÚNICA (no se duplica casa/centro)
> A diferencia de la Fase 0 (prerequisitos), aquí **no** se entrega dos veces. Se graba y se sube el vídeo **una sola vez**: el trabajo va a un **repositorio**, y duplicar casa/centro generaría conflictos. El criterio de almacenaje digital es el mismo de siempre.

---

## Índice de fases

| Fase | Carpeta | Qué aprende Marko |
|---|---|---|
| **1** | [fase-1-fundamentos](fase-1-fundamentos/README.md) | Instalar Git, identidad, `init`, commits, subir a GitHub |
| **2** | [fase-2-ramificacion](fase-2-ramificacion/README.md) | Ramas (`branch`, `merge`) — clave para trabajar en **binomio** |
| **3** | [fase-3-colaboracion](fase-3-colaboracion/README.md) | Colaborar con Carlos/Lucía: *pull requests*, conflictos |
| **4** | [fase-4-workflows](fase-4-workflows/README.md) | Flujos de trabajo profesionales |
| **5** | [fase-5-integracion](fase-5-integracion/README.md) | Integración y cierre |

> [!note] No todo es obligatorio para todos
> El **núcleo** (Fase 1: init, commit, push, pull, clone) lo hará todo el mundo. Las **ramas y colaboración** (Fases 2-3) cobran sentido sobre todo cuando trabajéis en **binomio** compartiendo un repositorio. El resto es material de ampliación. El profesor indicará qué parte toca en cada momento.
