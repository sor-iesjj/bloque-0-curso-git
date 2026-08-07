# 🛠️ Antes de empezar — prepara tu sitio de trabajo

> **Módulo:** SOR — Sistemas Operativos en Red · **Bloque 0 · Curso de Git**
>
> **📍 Cuándo se lee:** **AHORA.** Antes de la Fase 1.
>
> **⏱️ Te lleva:** unos 20 minutos.

---

> [!danger] 🛑 No abras la Fase 1 sin haber hecho esto
> Aquí dejas listas las **cuatro** cosas que vas a usar durante todo el curso: **el material**, **tu cuaderno**, **la bóveda de Marko** y **tu playlist**.
>
> Si empiezas sin esto, en el primer ejercicio te van a pedir que abras una entrada de apuntes y que trabajes en la bóveda de Marko… **y no vas a tener ninguna de las dos.**

---

## **1 · DE DÓNDE VIENES**

Este curso **no empieza de cero**. Das por hecho que ya tienes:

| Ya deberías tener | De dónde sale |
| :--- | :--- |
| Una **cuenta de GitHub** con Git instalado y SSH configurado | **Bloque 0 · Fase 0.2** |
| Tu **bóveda** `Boveda_SOR` en Obsidian | **Bloque 0 · Fase 0.1** |
| Tu **repositorio de apuntes** `apuntes-sor-t1` | **Bloque 0 · Fase 0.3** |

> [!warning] ⚠️ Si te falta alguna de las tres, para aquí
> Vuelve a los prerrequisitos y termínalos. **Este curso los usa desde el primer ejercicio.**
>
> *(Si llegas a este curso sin prerrequisitos —por traslado o incorporación tardía—, el `EJ-01-01-01` te los cubre.)*

---

## **2 · 🛑 LOS TRES SITIOS, Y POR QUÉ NO SE MEZCLAN**

Este es el punto donde más gente se lía. **Léelo despacio: son tres sitios distintos y cada uno tiene su dueño.**

```
📁 Tu carpeta personal
│
├── Boveda_SOR/                      ← 🎓 TU trabajo del curso
│   ├── 00_Apuntes/
│   │   └── Trimestre_1/                 ← repositorio 'apuntes-sor-t1'
│   │       ├── B0_Prerrequisitos/
│   │       └── B0_Curso_Git/            ← 🆕 la creas hoy: TUS entradas
│   │
│   └── 01_Practicas/
│       └── B0_Curso_Git/                ← 🆕 la clonas hoy: ESTE material
│
└── Boveda_Marko/                    ← 🎭 el mundo de Marko (ficticio)
    ├── Bitacora/                        ← repositorio propio, lo crea Marko
    └── Manuales/                        ← repositorio propio, lo crea Marko
```

> [!danger] 🛑 `Boveda_Marko` va FUERA de `Boveda_SOR`. No es negociable
> Y hay dos razones técnicas, las dos las vas a entender en este curso:
>
> | Si la metes dentro… | Lo que pasa |
> | :--- | :--- |
> | Dentro de un **repositorio** *(como `B0_Curso_Git`)* | **Git dentro de Git.** Los repos de Marko quedarían tragados por el repo del curso y no podrías subirlos por separado |
> | Dentro de la **bóveda** `Boveda_SOR` | **Obsidian dentro de Obsidian.** Dos bóvedas anidadas se pisan la configuración |
>
> Son **hermanas**, no una dentro de otra.

> [!info] 🎓 Por qué Marko tiene su propia bóveda
> Porque en este curso **rompes cosas a propósito**: borras ramas, provocas conflictos, deshaces commits, fuerzas `push`. Eso no se hace sobre tus apuntes de verdad.
>
> Marko es tu campo de pruebas. **Lo que aprendas ahí es exactamente lo que vas a aplicar en tu bóveda real** — pero si algo explota, explota en casa de Marko.

---

## **3 · 🔴 PASO 1 — TRAE ESTE CURSO A TU ORDENADOR**

El material vive en un **repositorio plantilla** mío. Tú **sacas tu propia copia** y la clonas.

### **3A · Saca tu copia en GitHub**

1. Abre el repositorio del curso: **`github.com/sor-iesjj/bloque-0-curso-git`**
2. Pulsa el botón verde **`Use this template`** → **`Create a new repository`**
3. **Repository name:** `bloque-0-curso-git` *(déjalo igual)*
4. Ponlo **público** o **privado**, como prefieras
5. **`Create repository`**

> [!info] 🎓 Qué acaba de pasar
> Ese repositorio **ya no es mío: es tuyo.** Tiene su propio historial y puedes escribir, romper y subir sin pedirle permiso a nadie. Es lo mismo que hiciste en la **Bloque 0 · Fase 0.4** con Boochan.

### **3B · Clónalo en tu bóveda**

```bash
cd ~/Boveda_SOR/01_Practicas
git clone git@github.com:TU-USUARIO/bloque-0-curso-git.git B0_Curso_Git
cd B0_Curso_Git
ls
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
> **Si lo omites**, Git le pone el nombre del repositorio y tendrías **la misma cosa con dos nombres**. Ya usaste el segundo argumento en la **Bloque 0 · Fase 0.3**, cuando clonaste `apuntes-sor-t1` y le dijiste que se llamara `Trimestre_1`.

> [!info] 🎓 ¿Por qué el repositorio se llama de otra manera?
> Porque **GitHub obliga**: los nombres de repositorio van en minúsculas y con guiones, no admite `B0_Curso_Git`.
>
> | Dónde vive | Cómo se llama |
> | :--- | :--- |
> | **En GitHub**, el repositorio | `bloque-0-curso-git` *(me lo impone GitHub)* |
> | **En tu ordenador**, la carpeta | `B0_Curso_Git` *(lo decides tú)* |
>
> **Dentro de tu bóveda, una cosa tiene un nombre y solo uno**: apuntes, práctica y playlist se llaman las tres `B0_Curso_Git`.

- **✅ Bien:** el `ls` muestra `00_INDICE.md`, `02_ENTREGABLES.md` y las cinco carpetas `fase-…`.
- **❌ Mal:** *"Permission denied (publickey)"* → tu SSH no está configurado. Vuelve a la **Bloque 0 · Fase 0.2.2**.

---

## **4 · 🔴 PASO 2 — PREPARA TU CUADERNO**

Tus apuntes **NO van en la carpeta del curso** ni en la bóveda de Marko. Van en tu repositorio de apuntes:

```bash
cd ~/Boveda_SOR/00_Apuntes/Trimestre_1
mkdir -p B0_Curso_Git
git status
```

- **✅ Bien:** ves `B0_Curso_Git` creada y `git status` responde.
- **❌ Mal:** *"not a git repository"* → **te has equivocado de carpeta.** `Trimestre_1` es tu repositorio `apuntes-sor-t1`; si Git no lo reconoce, estás fuera.

> [!danger] 🛑 No sigas hasta que `git status` responda
> Si no, escribirás 68 entradas de apuntes que no se van a subir a ninguna parte.

---

## **5 · 🔴 PASO 3 — CREA LA BÓVEDA DE MARKO**

**Vacía y hermana de tu bóveda**, como viste en el árbol del punto 2:

```bash
cd ~
mkdir -p Boveda_Marko
ls
```

- **✅ Bien:** ves `Boveda_Marko` **al lado** de `Boveda_SOR`, no dentro.

> [!warning] ⚠️ Aquí NO se hace `git init`. Todavía no, y nunca sobre la bóveda entera
> `Boveda_Marko/` es solo el contenedor. Los repositorios serán las carpetas de dentro —`Bitacora/` y `Manuales/`— y **las crea Marko durante los ejercicios**, no tú ahora.
>
> Es la misma regla de oro de tu bóveda real: **la bóveda no se versiona; se versionan las carpetas de dentro.**

**Ábrela en Obsidian** como una bóveda más: `Abrir carpeta como bóveda` → `Boveda_Marko`. Vas a tener dos bóvedas y podrás cambiar entre ellas.

---

## **6 · 🔴 PASO 4 — COMPRUEBA QUE PUEDES ENTREGAR**

**No esperes al primer ejercicio para descubrir que algo no funciona.** Recorrido completo con un fichero que no importa:

```bash
cd ~/Boveda_SOR/00_Apuntes/Trimestre_1
echo "# Prueba del curso de Git" > B0_Curso_Git/prueba.md

git add B0_Curso_Git/
git commit -m "Curso Git: prueba de que puedo subir apuntes"
git push
```

**Abre `github.com/TU-USUARIO/apuntes-sor-t1` en el navegador.**

- **✅ Bien:** ves `B0_Curso_Git` con `prueba.md` dentro.
- **❌ Mal:** si el `push` falla, **arréglalo hoy**. Es el mismo problema que tendrás en los 68 ejercicios.

**Y ahora borra el fichero de prueba**, que ya ha cumplido:

```bash
rm B0_Curso_Git/prueba.md
git add B0_Curso_Git/
git commit -m "Curso Git: quito el fichero de prueba"
git push
```

> [!success] 🎯 Por qué te hago esto antes de empezar
> Porque **acabas de comprobar el circuito entero** —escribir, añadir, confirmar, subir y verlo en GitHub— **con algo que no importa**.
>
> El día que falle, fallará con un fichero de prueba y no con el trabajo de tres horas.

---

## **7 · LA PLAYLIST**

Créala hoy, vacía, con este nombre exacto:

```
B0_Curso_Git
```

**No listada.** **Una sola para todo el curso** — no hagas una por fase: el vídeo ya lleva la fase en su nombre (`B0.G.1.2.1`) y salen ordenados solos.

---

## **8 · CÓMO VA A SER TU DÍA A DÍA**

```
1. Abres el ejercicio en   01_Practicas/B0_Curso_Git/fase-N-…/EJ-….md
2. Abres tu entrada en     00_Apuntes/Trimestre_1/B0_Curso_Git/git-….md
   (el nombre te lo da el propio ejercicio, en su Paso 0)
3. Grabas con OBS y haces el ejercicio en la bóveda de Marko
4. Escribes tus apuntes MIENTRAS trabajas, no al final
5. Subes el vídeo a B0_Curso_Git y pegas su enlace en la entrada
6. git add → git commit → git push  (en TU repositorio de apuntes)
```

> [!important] 📌 Fíjate en el paso 3 y el paso 6: son repositorios distintos
> **Trabajas** en los repos de Marko. **Entregas** en el tuyo. Cada `push` sabe a dónde va porque lo lanzas desde dentro de su carpeta.
>
> Cuando dudes de dónde estás: **`pwd`**. Es el reflejo que te va a salvar todo el curso.

---

## ✅ **CHECKLIST — no pases a la Fase 1 sin esto**

- [ ] Tengo mi copia del curso en GitHub *(`Use this template`)*.
- [ ] La he clonado en `01_Practicas/B0_Curso_Git/` y el `ls` muestra las cinco fases.
- [ ] He creado `00_Apuntes/Trimestre_1/B0_Curso_Git/`.
- [ ] `git status` me responde desde `Trimestre_1`.
- [ ] He creado `Boveda_Marko/` **fuera** de `Boveda_SOR`, y la abro en Obsidian.
- [ ] **Prueba de entrega hecha**: fichero → `add` → `commit` → `push` → **visto en GitHub**.
- [ ] He borrado el fichero de prueba y he subido el borrado.
- [ ] Playlist **`B0_Curso_Git`** creada, No listada.
- [ ] He leído **[📦 Entregables](02_ENTREGABLES.md)** y sé cómo se llama cada entrada.

---

> [!summary] 🎓 Qué has dejado listo
> **El material** en `01_Practicas/`, **tu cuaderno** en `00_Apuntes/`, **el campo de pruebas de Marko** aparte, y **comprobado que puedes subir a GitHub**.
>
> **Siguiente:** [📦 Qué tienes que entregar](02_ENTREGABLES.md) — cinco minutos y ya empiezas.
