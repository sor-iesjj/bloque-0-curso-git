# 🧯 Si lo rompes todo — borra la bóveda de Marko y vuelve a montarla

> **Módulo:** SOR — Sistemas Operativos en Red · **Bloque 0 · Curso de Git**
>
> **📍 Cuándo se lee:** cuando un repositorio de la bóveda de Marko ha quedado en un estado del que no sabes salir.

---

> [!info] 🎓 Para esto existe la bóveda de Marko
> Estás aprendiendo. Vas a dejar un `rebase` a medias, a borrar la rama que no era o a no entender qué te está diciendo Git. **No pasa nada**: `Boveda_Marko` está hecha para poder tirarla.
>
> Y fíjate en lo que vas a hacer para recuperarla: **bajar de GitHub lo que habías subido.** Es lo mismo que hiciste en la **Bloque 0 · Fase 0.7.2**, y es el motivo por el que un técnico hace `push` a menudo.

---

## **1 · ANTES DE BORRAR: PRUEBA ESTO**

Borrar es el último recurso. **Lee primero el mensaje de Git**, que casi siempre dice cómo salir:

| Lo que te pasa | Cómo se sale |
| :--- | :--- |
| Un `merge` se ha parado con conflictos y no quieres seguir | `git merge --abort` |
| Un `rebase` se ha parado y no quieres seguir | `git rebase --abort` |
| Un `cherry-pick` se ha parado | `git cherry-pick --abort` |
| Has cambiado ficheros y quieres dejarlos como en el último commit | `git restore .` |
| La terminal no responde y abajo hay un `:` | Es el paginador: pulsa **`q`** |
| No sabes en qué estado estás | `git status` — léelo entero, dice qué hacer |

**Si con eso no sales, sigue.**

---

## **2 · 🛑 QUÉ SE RECUPERA Y QUÉ NO**

| | ¿Se recupera? |
| :--- | :--- |
| Todo lo que habías subido con `git push` | ✅ **Sí.** Está en GitHub |
| Los commits que hiciste y **no** subiste | ❌ **No.** Solo existían en tu ordenador |
| Los cambios sin commit | ❌ **No** |
| Los vídeos | ✅ **Sí.** Están en YouTube, no en la bóveda |
| El *hook* `commit-msg` del `EJ-04-02-05` | ❌ **No.** Vive dentro de `.git/`, que no se sube: repite ese ejercicio |
| Los alias y la identidad de Git (`git config --global`) | ✅ **Sí.** No están en la bóveda, están en tu usuario |

> [!warning] ⚠️ Si tienes una entrada de la bitácora a medias, sálvala antes
> Abre el fichero en Obsidian, **copia el texto** y pégalo en un sitio fuera de `Boveda_Marko` (el Bloc de notas vale). Lo vuelves a pegar al terminar.

---

## **3 · 🔴 PASO 1 — BORRA LA BÓVEDA DE MARKO**

1. **Cierra Obsidian** y todas las terminales.
2. Abre el **Explorador de archivos** y navega hasta tu carpeta **`SOR`**.
3. **Clic derecho sobre la carpeta `SOR`** → `Abrir Git Bash aquí`.
4. **Comprueba dónde estás. Este `pwd` es el más importante del curso:**

```bash
pwd
ls
```

- **✅ Sigue solo si** la ruta termina en `/SOR` y el `ls` muestra **las dos**: `Boveda_Marko` y `Boveda_SOR`.

5. Borra **solo** la de Marko:

```bash
rm -rf Boveda_Marko
ls
```

- **✅ Bien:** el `ls` ya no muestra `Boveda_Marko`, y **`Boveda_SOR` sigue ahí**.

> [!danger] 🛑 Lee la orden dos veces antes de pulsar Intro
> `rm -rf` no pregunta y no pasa por la papelera. Lo que se escribe detrás es lo que desaparece. **Tiene que poner `Boveda_Marko`, y nada más.**
>
> Si prefieres no usar la terminal para esto, borra la carpeta `Boveda_Marko` desde el Explorador de archivos: hace lo mismo y sí pasa por la papelera.

---

## **4 · 🔴 PASO 2 — VUELVE A MONTARLA DESDE GITHUB**

En la misma terminal, que sigue en `SOR`:

```bash
mkdir Boveda_Marko
cd Boveda_Marko
pwd
```

- **✅ Bien:** la ruta termina en `/SOR/Boveda_Marko`.

Y baja tus tres repositorios. **Cambia `TU-USUARIO` por tu usuario de GitHub**, y no quites el nombre de carpeta del final de cada línea:

```bash
git clone git@github.com:TU-USUARIO/bloque-0-curso-git.git B0_Curso_Git
git clone git@github.com:TU-USUARIO/bitacora-curso-git.git Bitacora
git clone git@github.com:TU-USUARIO/manuales-boochan.git Manuales
ls
```

- **✅ Bien:** el `ls` muestra `B0_Curso_Git`, `Bitacora` y `Manuales`.

> [!info] 🎓 ¿Y si todavía no habías creado `manuales-boochan`?
> Ese repositorio se sube a GitHub en el `EJ-01-01-05`. Si lo rompiste antes, la tercera línea dará *"Repository not found"*: es normal. Deja las dos primeras y **repite los ejercicios `EJ-01-01-03` y `EJ-01-01-04`**, que son los que crean `Manuales`.

> [!info] 🎓 Por qué aquí no hay `git init` ni `git remote add`
> Porque al clonar, **el remoto ya viene configurado**. `git init` y `git remote add` son para una carpeta que nace en tu ordenador; `git clone` es para una que ya existe en GitHub.

---

## **5 · 🔴 PASO 3 — COMPRUEBA QUE HA VUELTO TODO**

```bash
cd Manuales
git remote -v
git log --oneline
git branch -a
cd ../Bitacora
git remote -v
git log --oneline
```

- **✅ Bien:** en `Manuales` el remoto nombra `manuales-boochan` y el `log` muestra tus commits; en `Bitacora` el remoto nombra `bitacora-curso-git` y están tus entradas.

> [!warning] ⚠️ Tus otras ramas están, pero hay que pedirlas
> Un clon recién hecho solo trae **abierta** la rama principal. Las demás aparecen en `git branch -a` como `remotes/origin/…`. Para volver a trabajar en una:
>
> ```bash
> git switch develop
> ```
>
> Git la crea en local a partir de la de GitHub. *(Las ramas se ven en la Fase 2; si aún no has llegado, ignora este aviso.)*

Por último, **abre otra vez `Boveda_Marko` en Obsidian** (`Abrir carpeta como bóveda`).

---

## **6 · Y DESPUÉS**

Vuelve al ejercicio en el que estabas y **empiézalo desde su Paso 0**. Lo que hubieras hecho en él sin subir, se repite.

> [!success] 🎯 Lo que acabas de comprobar
> Que **perder una carpeta no es perder el trabajo** si estaba subido.
>
> Y lo contrario también: lo que no llegó a GitHub **no ha vuelto**. Apunta en tu bitácora qué habías dejado sin subir y cuánto te ha costado rehacerlo. Es la mejor razón que vas a tener nunca para hacer `push` al terminar cada ejercicio.

---

> [!summary] 🎓 Qué has aprendido
> A distinguir entre **arreglar** un repositorio (los `--abort` y `git restore`) y **reponerlo** desde GitHub; y que reponerlo solo devuelve lo que estaba subido.
>
> **Vuelve a:** [🧭 Índice del curso](00_INDICE.md).
