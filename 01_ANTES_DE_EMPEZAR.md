# 🛠️ Antes de empezar — prepara tu sitio de trabajo

> **Módulo:** SOR — Sistemas Operativos en Red · **Bloque 0 · Curso de Git**
>
> **📍 Cuándo se lee:** **AHORA.** Antes de la Fase 1.
>
> **⏱️ Te lleva:** unos 20 minutos.

---

> [!danger] 🛑 No abras la Fase 1 sin haber hecho esto
> Aquí dejas listas las **cuatro** cosas que vas a usar durante todo el curso: **la bóveda de Marko**, **el material**, **tu bitácora** y **tu playlist**.
>
> Si empiezas sin esto, en el primer ejercicio te van a pedir que abras una entrada en tu bitácora y que trabajes en la bóveda de Marko… **y no vas a tener ninguna de las dos.**

---

## **1 · DE DÓNDE VIENES**

Este curso **no empieza de cero**. Das por hecho que ya tienes:

| Ya deberías tener | De dónde sale |
| :--- | :--- |
| Una carpeta **`SOR`** con tu bóveda `Boveda_SOR` dentro | **Bloque 0 · Fase 0.1** |
| Una **cuenta de GitHub** con Git instalado y SSH configurado | **Bloque 0 · Fase 0.2** |
| Haber creado ya **un repositorio desde cero** y haberlo subido | **Bloque 0 · Fase 0.3** |

> [!warning] ⚠️ Si te falta alguna de las tres, para aquí
> Vuelve a los prerrequisitos y termínalos. **Este curso los usa desde el primer paso de esta página.**

---

## **2 · 🛑 LA REGLA DE ESTE CURSO: `Boveda_SOR` NO SE TOCA**

**Todo el curso de Git ocurre dentro de otra bóveda, `Boveda_Marko`.** El material, tus apuntes y los experimentos: los tres.

```
📁 SOR/                          ← la carpeta que creaste en la Bloque 0 · Fase 0.1
│
├── Boveda_SOR/                  ← 🔒 tu trabajo real. EN ESTE CURSO NO SE TOCA
│
└── Boveda_Marko/                ← 🎭 el curso de Git ENTERO vive aquí
    ├── B0_Curso_Git/                ← 📖 el material: los enunciados que lees
    ├── Bitacora/                    ← ✍️ tus apuntes: lo que entregas
    └── Manuales/                    ← 🛠️ los experimentos: donde se rompen cosas
```

> [!info] 🎓 Por qué te hago trabajar en otra bóveda
> Porque en este curso **rompes cosas a propósito**: borras ramas, provocas conflictos, deshaces commits, fuerzas un `push`. Y además estás aprendiendo, así que también vas a romper cosas **sin querer**.
>
> Si eso pasa en `Boveda_Marko`, no pasa nada: **se borra entera y se vuelve a montar desde GitHub** (está explicado en [🧯 Si lo rompes todo](03_SI_LO_ROMPES_TODO.md)). Si pasara en `Boveda_SOR`, te llevarías por delante los apuntes de todo el trimestre.
>
> **Por eso durante todo este curso no abres una terminal dentro de `Boveda_SOR`. Ni una vez.**

**Dentro de `Boveda_Marko` hay tres carpetas, y cada una es un repositorio distinto:**

| Carpeta | Qué haces en ella | Repositorio en GitHub | Cuándo la creas |
| :--- | :--- | :--- | :--- |
| `B0_Curso_Git/` | **Leer** los enunciados | `bloque-0-curso-git` | Hoy, en el Paso 2 |
| `Bitacora/` | **Escribir** tus apuntes y **entregarlos** | `bitacora-curso-git` | Hoy, en el Paso 3 |
| `Manuales/` | **Ejecutar** los ejercicios | `manuales-boochan` | En el `EJ-01-01-03`, ya dentro del curso |

> [!danger] 🛑 `Boveda_Marko` es solo el contenedor: ahí NUNCA se hace `git init`
> Es la misma regla de oro de tu bóveda real: **la bóveda no se versiona; se versionan las carpetas de dentro.** Si hicieras `git init` en `Boveda_Marko`, los tres repositorios quedarían unos dentro de otros —**Git dentro de Git**— y no podrías subirlos por separado.

---

## **3 · 🔴 PASO 1 — CREA LA BÓVEDA DE MARKO**

**No teclees la ruta:** la carpeta `SOR` de cada uno está en un sitio distinto (lo viste en la **Bloque 0 · Fase 0.1**). Haz lo mismo que en la **Bloque 0 · Fase 0.3**:

1. Abre el **Explorador de archivos** y navega hasta tu carpeta **`SOR`** — la que tiene `Boveda_SOR` dentro.
2. **Clic derecho sobre la carpeta `SOR`** (o dentro de ella, en un hueco vacío):
   - **Windows:** `Abrir Git Bash aquí` / `Git Bash Here`. En Windows 11 puede estar dentro de **`Mostrar más opciones`**.
   - **Linux:** `Abrir en un terminal`.
3. **Comprueba dónde has caído** antes de tocar nada:

```bash
pwd
ls
```

- **✅ Bien:** la ruta termina en `/SOR` y el `ls` muestra `Boveda_SOR`.
- **❌ Mal:** si la ruta termina en `Boveda_SOR` o en algo de dentro, **te has pasado de carpeta**. Cierra esa terminal y ábrela sobre `SOR`.

4. Ahora sí, crea la bóveda y entra en ella:

```bash
mkdir Boveda_Marko
cd Boveda_Marko
pwd
```

- **✅ Bien:** la ruta termina en `/SOR/Boveda_Marko`. **En la ruta no aparece `Boveda_SOR`.**

> [!warning] ⚠️ Aquí NO se hace `git init`
> `Boveda_Marko` es el contenedor. Los repositorios son las carpetas que vas a meter dentro en los pasos siguientes.

**No cierres esta terminal:** los Pasos 2 y 3 siguen desde aquí.

---

## **4 · 🔴 PASO 2 — TRAE EL MATERIAL DEL CURSO**

El material vive en un **repositorio plantilla** mío. Tú **sacas tu propia copia** y la clonas, igual que hiciste en la **Bloque 0 · Fase 0.4.a**.

### **4A · Saca tu copia en GitHub**

1. Abre el repositorio del curso: **`github.com/sor-iesjj/bloque-0-curso-git`**
2. Pulsa el botón verde **`Use this template`** → **`Create a new repository`**
3. **Repository name:** `bloque-0-curso-git` *(déjalo igual)*
4. Ponlo **público** o **privado**, como prefieras
5. **`Create repository`**

### **4B · Clónalo dentro de la bóveda de Marko**

En la terminal del Paso 1, que sigue en `Boveda_Marko`:

```bash
pwd
git clone git@github.com:TU-USUARIO/bloque-0-curso-git.git B0_Curso_Git
ls B0_Curso_Git
```

> [!warning] ⚠️ Cambia `TU-USUARIO` por tu usuario de GitHub
> El resto de la línea, **tal cual**. Incluido el `B0_Curso_Git` del final.

> [!important] 📌 El `B0_Curso_Git` del final no está de adorno
> Es el **segundo argumento** de `git clone`, y decide **cómo se llama la carpeta** en tu ordenador:
>
> ```
> git clone  <dirección del repositorio>  <nombre de la carpeta>
> ```
>
> **Si lo omites**, Git le pone el nombre del repositorio y tendrías **la misma cosa con dos nombres**. GitHub obliga a minúsculas y guiones (`bloque-0-curso-git`); en tu ordenador la carpeta se llama `B0_Curso_Git`, igual que la playlist.

- **✅ Bien:** el `pwd` termina en `/SOR/Boveda_Marko` y el `ls` muestra `00_INDICE.md`, `02_ENTREGABLES.md` y las cinco carpetas `fase-…`.
- **❌ Mal:** *"Permission denied (publickey)"* → tu SSH no está configurado. Vuelve a la **Bloque 0 · Fase 0.2.2**.

> [!info] 🎓 Esta carpeta es de solo lectura
> Aquí están los enunciados. **No ejecutas ejercicios dentro de `B0_Curso_Git`**: los lees aquí y los haces en `Manuales/`.

---

## **5 · 🔴 PASO 3 — CREA TU BITÁCORA**

Tu **bitácora** es el cuaderno del curso: una entrada por ejercicio. **Es lo que entregas y lo que corrijo.** Y es un repositorio que montas tú, con los mismos tres gestos de la **Bloque 0 · Fase 0.3**.

### **5A · La carpeta y el repositorio local**

En la misma terminal, que sigue en `Boveda_Marko`:

```bash
mkdir Bitacora
cd Bitacora
pwd
```

- **✅ Bien:** la ruta termina en `/SOR/Boveda_Marko/Bitacora`.

> [!danger] 🛑 El `pwd` va ANTES del `git init`, siempre
> `git init` convierte en repositorio **la carpeta en la que estás**, sea la que sea. Si lo lanzas un nivel más arriba, conviertes la bóveda entera.

```bash
git init
git branch -M main
git status
```

### **5B · El repositorio en GitHub**

1. En `github.com`, arriba a la derecha: **`+` → `New repository`**.
2. **Repository name:** `bitacora-curso-git` *(exacto, en minúsculas)*
3. **Visibility:** **`Private`**.
4. **⚠️ NO marques nada** de `Add a README file`, `Add .gitignore` ni `Choose a license`. Tiene que nacer **vacío**.
5. **`Create repository`** y copia la dirección **`SSH`**.

### **5C · Conéctalo**

```bash
git remote add origin git@github.com:TU-USUARIO/bitacora-curso-git.git
git remote -v
```

- **✅ Bien:** salen dos líneas con `origin` y las dos nombran `bitacora-curso-git`.

---

## **6 · 🔴 PASO 4 — COMPRUEBA QUE PUEDES ENTREGAR**

**No esperes al primer ejercicio para descubrir que algo no funciona.** Recorrido completo, con la portada de tu bitácora:

```bash
pwd
echo "# Bitácora del curso de Git" > README.md
git add README.md
git commit -m "Bitacora: portada"
git push -u origin main
```

**Abre `github.com/TU-USUARIO/bitacora-curso-git` en el navegador.**

- **✅ Bien:** ves el `README.md`.
- **❌ Mal:** si el `push` falla, **arréglalo hoy**. Es el mismo problema que tendrías en todos los ejercicios.

> [!success] 🎯 Por qué te hago esto antes de empezar
> Porque **acabas de comprobar el circuito entero** —escribir, añadir, confirmar, subir y verlo en GitHub— **con algo que no importa**.
>
> El día que falle, fallará con una portada de una línea y no con el trabajo de tres horas.

---

## **7 · PASO 5 — ABRE LA BÓVEDA DE MARKO EN OBSIDIAN**

En Obsidian: **`Abrir carpeta como bóveda`** → elige **`Boveda_Marko`**.

Vas a tener dos bóvedas y podrás cambiar entre ellas. En la de Marko ves las carpetas `B0_Curso_Git` (los enunciados) y `Bitacora` (tus entradas): **lees el ejercicio y escribes tus apuntes sin salir de la misma ventana.**

> [!warning] ⚠️ Se abre `Boveda_Marko`, no una carpeta de dentro
> Si abres `Bitacora` como bóveda, Obsidian guarda su configuración **dentro de tu repositorio** y acabará subiéndose a GitHub.

---

## **8 · 🛑 CÓMO SABER EN QUÉ REPOSITORIO ESTÁS**

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

## **9 · LA PLAYLIST**

Créala hoy, vacía, con este nombre exacto:

```
B0_Curso_Git
```

**No listada.** **Una sola para todo el curso** — no hagas una por fase: el vídeo ya lleva la fase en su nombre (`B0.G.1.2.1`) y salen ordenados solos.

---

## **10 · CÓMO VA A SER TU DÍA A DÍA**

```
1. Lees el ejercicio en      Boveda_Marko/B0_Curso_Git/fase-N-…/EJ-….md
2. Abres tu entrada en       Boveda_Marko/Bitacora/git-….md
   (el nombre te lo da el propio ejercicio, en su Paso 0)
3. Grabas con OBS y haces el ejercicio en   Boveda_Marko/Manuales
4. Escribes tus apuntes MIENTRAS trabajas, no al final
5. Subes el vídeo a B0_Curso_Git y pegas su enlace en la entrada
6. Cambias a Bitacora:  git add → git commit → git push
```

> [!important] 📌 Fíjate en el paso 3 y el paso 6: son repositorios distintos
> **Trabajas** en `Manuales`. **Entregas** desde `Bitacora`. Cada `push` sabe a dónde va porque lo lanzas desde dentro de su carpeta — y por eso antes de cada uno miras `git remote -v`.

---

## ✅ **CHECKLIST — no pases a la Fase 1 sin esto**

- [ ] He creado `Boveda_Marko` **dentro de `SOR`, al lado de `Boveda_SOR`**, y no he hecho `git init` en ella.
- [ ] Tengo mi copia del curso en GitHub *(`Use this template`)*.
- [ ] La he clonado en `Boveda_Marko/B0_Curso_Git/` y el `ls` muestra las cinco fases.
- [ ] He creado `Boveda_Marko/Bitacora/` y es un repositorio: `git status` me responde ahí dentro.
- [ ] `git remote -v` dentro de `Bitacora` nombra `bitacora-curso-git`.
- [ ] **Prueba de entrega hecha**: `README.md` → `add` → `commit` → `push` → **visto en GitHub**.
- [ ] Abro `Boveda_Marko` en Obsidian y veo `B0_Curso_Git` y `Bitacora`.
- [ ] Playlist **`B0_Curso_Git`** creada, No listada.
- [ ] He leído **[📦 Entregables](02_ENTREGABLES.md)** y sé cómo se llama cada entrada.
- [ ] Sé dónde está **[🧯 Si lo rompes todo](03_SI_LO_ROMPES_TODO.md)**.

---

> [!summary] 🎓 Qué has dejado listo
> **La bóveda de Marko** al lado de la tuya, con **el material** y **tu bitácora** dentro, y **comprobado que puedes subir a GitHub**. `Manuales`, el repositorio donde se hacen los ejercicios, lo creas tú en la Fase 1.
>
> Y `Boveda_SOR` cerrada: no se toca hasta que acabe este curso.
>
> **Siguiente:** [📦 Qué tienes que entregar](02_ENTREGABLES.md) — cinco minutos y ya empiezas.
