# 🛠️ Antes de empezar — cómo se trabaja en este curso

> **Módulo:** SOR — Sistemas Operativos en Red · **Bloque 0 · Curso de Git**
>
> **📍 Cuándo se lee:** **AHORA.** Antes de la Fase 1.

---

> [!important] 📌 Esta página es para leer. Aquí no se crea nada
> **Todo lo que hay que montar se monta en el primer ejercicio**, el [`EJ-01-01-00`](fase-1-fundamentos/EJ-01-01-00.md): la bóveda de Marko, la copia del material y tu bitácora. En su Paso 3 descargas el repositorio completo y lo abres en Obsidian. Se hace dentro del vídeo para que quede registrado.
>
> Esta página te explica **dónde va a estar cada cosa y por qué**, para que cuando lo montes sepas qué estás haciendo.

---

## **1 · DE DÓNDE VIENES**

Este curso **no empieza de cero**. De los prerrequisitos traes tres cosas, y el primer ejercicio las vuelve a comprobar una por una:

| Traes | De dónde sale |
| :--- | :--- |
| Una carpeta **`SOR`** con tu bóveda `Boveda_SOR` dentro | **Bloque 0 · Fase 0.1** |
| Git instalado y tu nombre y correo configurados | **Bloque 0 · Fase 0.2.1** |
| Tu clave SSH puesta en GitHub | **Bloque 0 · Fase 0.2.2** |

---

## **2 · 🛑 LA REGLA DE ESTE CURSO: `Boveda_SOR` NO SE TOCA**

**Todo el curso de Git ocurre dentro de otra bóveda, `Boveda_Marko`.** El material, tus apuntes y los ejercicios: los tres.

```
📁 SOR/                          ← la carpeta que creaste en la Bloque 0 · Fase 0.1
│
├── Boveda_SOR/                  ← 🔒 tu trabajo real. EN ESTE CURSO NO SE TOCA
│
└── Boveda_Marko/                ← 🎭 el curso de Git ENTERO vive aquí
    ├── B0_Curso_Git/                ← 📖 el material: los enunciados que lees
    ├── Bitacora/                    ← ✍️ tus apuntes: lo que entregas
    └── Manuales/                    ← 🛠️ los ejercicios: donde se rompen cosas
```

> [!info] 🎓 Por qué te hago trabajar en otra bóveda
> Porque en este curso **rompes cosas a propósito**: borras ramas, provocas conflictos, deshaces commits, fuerzas un `push`. Y además estás aprendiendo, así que también vas a romper cosas **sin querer**.
>
> Si eso pasa en `Boveda_Marko`, no pasa nada: **se borra entera y se vuelve a bajar de GitHub** (está explicado en [🧯 Si lo rompes todo](03_SI_LO_ROMPES_TODO.md)). Si pasara en `Boveda_SOR`, te llevarías por delante los apuntes de todo el trimestre.
>
> **Por eso durante todo este curso no abres una terminal dentro de `Boveda_SOR`. Ni una vez.**

**Dentro de `Boveda_Marko` hay tres carpetas, y cada una es un repositorio distinto:**

| Carpeta | Qué haces en ella | Repositorio en GitHub | En qué ejercicio la creas |
| :--- | :--- | :--- | :--- |
| `B0_Curso_Git/` | **Leer en Obsidian** los enunciados descargados | `bloque-0-curso-git` | `EJ-01-01-00`, Paso 3 |
| `Bitacora/` | **Escribir** tus apuntes y **entregarlos** | `bitacora-curso-git` | `EJ-01-01-00`, Pasos 4 a 6 |
| `Manuales/` | **Ejecutar** los ejercicios | `manuales-boochan` | `EJ-01-01-03`, y se sube a GitHub en el `EJ-01-01-05` |

> [!danger] 🛑 `Boveda_Marko` es solo el contenedor: ahí NUNCA se hace `git init`
> Es la misma regla de oro de tu bóveda real: **la bóveda no se versiona; se versionan las carpetas de dentro.** Si hicieras `git init` en `Boveda_Marko`, los tres repositorios quedarían unos dentro de otros —**Git dentro de Git**— y no podrías subirlos por separado.

---

## **3 · 🛑 CÓMO SABER EN QUÉ REPOSITORIO ESTÁS**

Vas a moverte entre `Manuales` y `Bitacora` en cada ejercicio. **La terminal no te avisa de que te has equivocado de carpeta: ejecuta lo que le escribas, donde estés.** Estas son las tres comprobaciones, de la más rápida a la más segura:

| # | Qué miras | Qué te dice |
| :--- | :--- | :--- |
| 1 | **La línea de Git Bash**, antes de escribir | Enseña la carpeta y, entre paréntesis, la rama: `…/Boveda_Marko/Manuales (main)` |
| 2 | `pwd` | La ruta completa de la carpeta en la que estás |
| 3 | `git remote -v` | **A qué repositorio de GitHub irá tu `push`** |

**La tercera es la que no falla.** Apréndete qué tiene que salir:

| Si estás en… | `git remote -v` nombra… |
| :--- | :--- |
| `Boveda_Marko/Manuales` | `manuales-boochan` |
| `Boveda_Marko/Bitacora` | `bitacora-curso-git` |
| `Boveda_Marko/B0_Curso_Git` | `bloque-0-curso-git` |

> [!danger] 🛑 Si en la ruta aparece `Boveda_SOR`, o el remoto nombra `apuntes-sor-t1`: PARA
> Estás en tu trabajo real. **No ejecutes nada.** Cierra esa terminal y ábrela sobre la carpeta correcta de `Boveda_Marko`.
>
> Cada ejercicio te recuerda esta comprobación al empezar, y otra vez delante de cada orden que no tiene vuelta atrás.

---

## **4 · CÓMO VA A SER TU DÍA A DÍA**

Desde el segundo ejercicio, todos se hacen igual:

```
1. Lees el ejercicio en      Boveda_Marko/B0_Curso_Git/fase-N-…/EJ-….md
2. Abres tu entrada en       Boveda_Marko/Bitacora/git-….md
   (el nombre te lo da el propio ejercicio, en su Paso 0)
3. Grabas con OBS y haces el ejercicio en   Boveda_Marko/Manuales
4. Escribes tus apuntes MIENTRAS trabajas, no al final
5. Subes el vídeo a la playlist B0_Curso_Git y pegas su enlace en la entrada
6. Cambias a Bitacora:  git add → git commit → git push
```

> [!important] 📌 Fíjate en el paso 3 y el paso 6: son repositorios distintos
> **Trabajas** en `Manuales`. **Entregas** desde `Bitacora`. Cada `push` sabe a dónde va porque lo lanzas desde dentro de su carpeta — y por eso antes de cada uno miras `git remote -v`.
>
> El último paso de cada ejercicio es esa entrega, ya escrita con su nombre de fichero: no tienes que acordarte de los comandos.

---

## **5 · EL ORDEN PARA EMPEZAR**

1. Lee [Entregables](02_ENTREGABLES.md) y el inicio del [`EJ-01-01-00`](fase-1-fundamentos/EJ-01-01-00.md) en el **PDF de arranque** que te facilite el profesor. Si todavía no lo tienes, puedes consultar esas páginas iniciales en `https://github.com/sor-iesjj/bloque-0-curso-git` hasta completar el Paso 3. Es la única lectura provisional: el curso aún no está descargado.
2. En el **Paso 2** de ese ejercicio, localiza tu carpeta `SOR` y crea `Boveda_Marko` **al lado de** `Boveda_SOR`.
3. En el **Paso 3**, entra en `https://github.com/sor-iesjj/bloque-0-curso-git`, crea tu copia con **«Use this template»** y clónala en `SOR/Boveda_Marko/B0_Curso_Git`. El ejercicio da los comandos y las comprobaciones exactas; grábalo como parte de la práctica.
4. Abre **`Boveda_Marko` como bóveda en Obsidian**. Dentro, entra en `B0_Curso_Git/00_INDICE.md`, vuelve a `fase-1-fundamentos/EJ-01-01-00.md` y continúa por el Paso 4 desde **la copia local**. El Paso 3 del ejercicio explica cómo comprobar que abriste la carpeta correcta.
5. Después sigue el [índice de la Fase 1](fase-1-fundamentos/README.md). Para los demás ejercicios leerás el material desde Obsidian; los PDF son un apoyo y GitHub sirve para obtener la copia y comprobar las entregas.

---

> [!summary] 🎓 Con qué te quedas
> **Una bóveda aparte, tres repositorios dentro, y `Boveda_SOR` cerrada** hasta que acabe el curso. Dónde estás lo dice `git remote -v`, no tu memoria.
>
> **Siguiente:** [📦 Qué tienes que entregar](02_ENTREGABLES.md), y de ahí al primer ejercicio.
