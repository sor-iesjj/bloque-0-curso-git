# 📦 Qué tienes que entregar — LÉEME ANTES DEL PRIMER EJERCICIO

> **Módulo:** SOR — Sistemas Operativos en Red · **Bloque 0 · Curso de Git**
>
> **📍 Cuándo se lee:** **AHORA.** Después de [🛠️ Antes de empezar](01_ANTES_DE_EMPEZAR.md) y antes de abrir la Fase 1.

---

> [!danger] 🛑 No empieces ningún ejercicio sin haber leído esta página
> Aquí está **todo lo que se te va a pedir**: dónde van tus apuntes, cómo se llaman, qué llevan dentro y cómo se entregan.
>
> Si empiezas a hacer ejercicios y dejas los apuntes "para luego", te va a pasar una de dos: o los escribes de memoria al final —y se nota— o los pierdes. **Las dos cuentan como no entregado.**

---

## **1 · LOS TRES ENTREGABLES DE CADA EJERCICIO**

Cada uno de los **68 ejercicios** produce **tres cosas**, y las tres van juntas:

| # | Entregable | Dónde vive |
| :--- | :--- | :--- |
| 1 | **Una entrada de apuntes** | Tu repositorio `apuntes-sor-t1`, en GitHub |
| 2 | **Un vídeo** | Tu playlist `B0_Curso_Git`, **No listado** |
| 3 | **El `push`** que sube la entrada | Tu repositorio de apuntes |

**No hay entrega parcial.** Un vídeo sin entrada no cuenta, y una entrada sin el enlace del vídeo tampoco.

> [!warning] ⚠️ El trabajo de Marko NO es un entregable
> En este curso trabajas en **la bóveda de Marko** —creas sus repos, los rompes, los arreglas—. Eso es **el ejercicio**, y queda demostrado en el vídeo.
>
> **Lo que se entrega es tu entrada de apuntes**, en tu repositorio. Los repos de Marko son tuyos y puedes hacer con ellos lo que quieras: nadie los va a corregir.

---

## **2 · DÓNDE VAN TUS APUNTES**

Dentro de tu bóveda, en esta ruta exacta:

```
00_Apuntes/Trimestre_1/B0_Curso_Git/
```

> [!warning] ⚠️ Esa carpeta la creaste en el paso 2 de [🛠️ Antes de empezar](01_ANTES_DE_EMPEZAR.md)
> Si no la tienes todavía, vuelve ahí y créala antes de seguir.
>
> *(Si tu bóveda usa otro trimestre porque te incorporaste más tarde, cambia el número. Lo que no cambia es `B0_Curso_Git`.)*

---

## **3 · CÓMO SE LLAMA CADA ENTRADA**

**Una entrada por ejercicio.** El nombre se construye siempre igual:

```
git-<fase>.<nivel>.<numero>-<titulo-en-minusculas-con-guiones>.md
```

**Ejemplos reales del curso:**

| Ejercicio | Fichero de apuntes |
| :--- | :--- |
| `EJ-01-02-01` — Marko amplía el manual | `git-1.2.1-amplia-el-manual-y-registra.md` |
| `EJ-02-01-01` — Marko crea su primera rama | `git-2.1.1-crea-su-primera-rama.md` |
| `EJ-03-01-01` — Marko da acceso a Carlos | `git-3.1.1-da-acceso-de-colaborador.md` |

> [!important] 📌 El nombre exacto te lo da cada ejercicio
> **No tienes que inventártelo.** Al principio de cada ejercicio, en el **Paso 0**, aparece el nombre que le toca. Cópialo tal cual.

> [!danger] ⚠️ Los nombres NO son orientativos
> Con un grupo entero entregando, si cada uno pone el nombre que le apetece **corregir se vuelve imposible y tu entrega se pierde**. Sin dramas y sin excepciones: el nombre es el que pone el ejercicio.

---

## **4 · 🔴 QUÉ LLEVA DENTRO CADA ENTRADA**

**Esta estructura es obligatoria.** Cópiala y rellénala:

```markdown
# git-1.2.1 · Marko amplía el manual y registra el cambio

- **Alumno:** Nombre Apellido
- **Fecha de inicio:** 2026-09-15
- **Fecha de entrega:** 2026-09-17
- **Fase:** 1 — Fundamentos
- **Nivel:** N2 — Notable
- **Ejercicio:** EJ-01-02-01

---

## 🎯 Qué se pedía

*(Dos o tres líneas con tus palabras: qué le encargaban a Marko y qué había que resolver.)*

---

## ⌨️ Comandos y pasos importantes

*(Los comandos de Git de este ejercicio, con una línea diciendo QUÉ HACE cada uno.
No pegues la terminal entera: quédate con los que importan.)*

```bash
git diff          # ver qué he cambiado antes de guardarlo
git add manual.md # marcar el fichero para el próximo commit
```

---

## 🛠️ Qué he hecho

*(Los pasos que has seguido. No copies el enunciado: cuenta lo que hiciste tú.)*

---

## 🚩 Qué me ha fallado y cómo lo he resuelto

*(Los errores que te han salido, con el mensaje literal, y qué hiciste.
Si no te falló nada, escribe "nada" — pero piénsalo dos veces antes.)*

---

## 🤔 Respuestas a las preguntas

*(Las preguntas del apartado de verificación del ejercicio, con tus palabras.
Copiar del enunciado NO cuenta como respuesta.)*

**1.**
**2.**
**3.**

---

## 🔗 Enlaces

- **Vídeo de esta práctica:**
- **Playlist del curso:** `B0_Curso_Git`
- **Repositorio de Marko usado hoy:**

---

## 💭 Dudas / a repasar

*(Lo que no te ha quedado claro.)*
```

> [!success] 🎯 Esta estructura es la MISMA en todo el curso
> La misma en prerrequisitos, en el curso de Shell y en Boochan. **Se aprende una vez y se repite doscientas** — la viste por primera vez en la **Bloque 0 · Fase 0.1**.
>
> Y en Git el apartado de comandos es el que más te va a servir: `git reset`, `git revert` y `git checkout` suenan parecido y hacen cosas muy distintas. **Es tu chuleta, escrita por ti**, y la vas a usar todo el año.

> [!warning] ⚠️ El apartado que más se deja vacío es el de los fallos
> Y es el que más dice de ti. **Un ejercicio donde todo salió a la primera es casi siempre un ejercicio que no se ha entendido**, o uno donde se copió y pegó sin mirar.
>
> Anota el mensaje de error **literal**. Te servirá a ti dentro de tres semanas y a un compañero la semana que viene.

> [!info] 📅 Por qué se piden las dos fechas
> Porque **un ejercicio puede durarte varios días**, y eso es normal. **Lo que no se hace es abrir una entrada nueva cada día.** Abres la del ejercicio el primer día y sigues escribiendo en ella hasta terminarlo.
>
> **Una entrada = un ejercicio**, dure lo que dure.

---

## **5 · LOS VÍDEOS**

| | |
| :--- | :--- |
| **Playlist** | `B0_Curso_Git` — **una sola para todo el curso**, No listada |
| **Nombre** | `B0.G.<fase>.<nivel>.<num> · <título>` — ej. `B0.G.1.2.1 · Marko amplía el manual y registra el cambio` |
| **Duración** | Lo que dure el ejercicio. Ni se alarga ni se corta |
| **Timestamps** | `00:00 Presentación` y **uno por paso** |

> [!danger] 🛑 Identifícate al empezar CADA vídeo
> Tu perfil de GitHub, tu Teams o tu correo `@alu.edu.gva.es` **en pantalla**. Y di tu nombre en voz alta.
>
> **Es corte duro:** un vídeo sin identificación no cuenta, aunque el ejercicio esté perfecto.

> [!info] 🎬 Una sola playlist, y no una por fase
> El vídeo ya lleva la fase en su nombre (`B0.G.**3**.1.1`), así que dentro de la playlist salen ordenados solos. Doce playlists en el Bloque 0 no las encuentra nadie, empezando por ti.

---

## **6 · ENTREGA ÚNICA — ESTO NO SE DUPLICA CASA/CENTRO**

A diferencia de los prerrequisitos, aquí **no se entrega dos veces**. Grabas y subes el vídeo **una sola vez**, y haces **un solo `push`**.

> [!info] 🎓 Por qué
> Porque el trabajo va a **un repositorio**. Duplicar la entrega casa/centro sobre el mismo repo genera conflictos — que, por cierto, es justo lo que vas a aprender a resolver en la **Fase 3**.

---

## **7 · CÓMO SE ENTREGA**

1. **Escribe tu entrada mientras trabajas**, no al terminar.
2. **Sube el vídeo** a `B0_Curso_Git` y **pega su enlace dentro de la entrada**.
3. **Sube la entrada**, desde tu repositorio de apuntes:

```bash
cd ~/Boveda_SOR/00_Apuntes/Trimestre_1
git add B0_Curso_Git/
git commit -m "Curso Git: EJ-01-02-01 terminado"
git push
```

4. **Compruébalo en GitHub con tus ojos.** Que el `push` no dé error no significa que esté donde crees.

> [!danger] 🛑 El `push` se hace desde `Trimestre_1`, no desde la bóveda de Marko
> Es el error nº1 de este curso: hacer el `push` estando dentro de un repo de Marko y no entender por qué la entrada no aparece.
>
> **Cuando dudes: `pwd`.**

---

## ✅ **RESUMEN — pégatelo donde lo veas**

```
POR CADA EJERCICIO
├── APUNTES   00_Apuntes/Trimestre_1/B0_Curso_Git/git-f.n.e-titulo.md
│              escrita MIENTRAS trabajas, con la estructura del punto 4
├── VÍDEO     playlist "B0_Curso_Git", No listado, con timestamps
│              nombre: B0.G.f.n.e · Título   ·   identifícate al empezar
└── PUSH      desde Trimestre_1 (¡no desde la bóveda de Marko!)
               y comprobado en GitHub
```

---

> [!summary] 🎓 Y ahora sí, a empezar
> **Siguiente:** [🧭 Índice del curso](00_INDICE.md) → **Fase 1**.
