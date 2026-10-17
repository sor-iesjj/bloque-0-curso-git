# Recuperar el recorrido de Git — Cole o Casa

> Usa esta guía solo si no puedes reparar el repositorio con `git status` y los mensajes de Git. Recupera **un contexto cada vez**.

> [!danger] Antes de borrar
> Los cambios sin `commit` o sin `push` pueden perderse. Copia fuera de la bóveda cualquier entrada de bitácora que necesites conservar. No borres la otra bóveda ni carpetas de `Boveda_SOR`.

## 1. Elige un único contexto

| Recorrido | Bóveda | Bitácora remota | Manuales remoto |
|---|---|---|---|
| Cole | `Boveda_Git_Cole` | `bitacora-curso-git-cole` | `manuales-boochan-cole` |
| Casa | `Boveda_Git_Casa` | `bitacora-curso-git-casa` | `manuales-boochan-casa` |

Cierra Obsidian y abre una terminal en la carpeta `SOR`. Antes de borrar, comprueba la ruta y las dos bóvedas:

```bash
pwd
ls
```

Continúa solo si `pwd` termina en `/SOR` y puedes identificar con claridad la bóveda del contexto que elegiste. Si `Boveda_SOR` existe, no la borres ni la modifiques; no es requisito que esté presente en este ordenador. Si dudas, para.

## 2. Borra solo la bóveda elegida

Para Cole, sustituye el valor por `Boveda_Git_Cole`. Para Casa, usa `Boveda_Git_Casa`. Ejecuta únicamente la línea que corresponde a tu contexto:

```bash
rm -rf Boveda_Git_Cole
```

```bash
rm -rf Boveda_Git_Casa
```

Comprueba con `ls` que desapareció la bóveda elegida y que la otra sigue intacta. Esta orden no pasa por la papelera.

## 3. Vuelve a crear y clonar los repositorios de ese contexto

Dentro de la misma carpeta `SOR`, elige **un solo bloque**. Sustituye `TU-USUARIO` por tu usuario real de GitHub.

**Cole:**

```bash
mkdir Boveda_Git_Cole
cd Boveda_Git_Cole
git clone https://github.com/sor-iesjj/bloque-0-curso-git.git B0_Curso_Git_Cole
git clone git@github.com:TU-USUARIO/bitacora-curso-git-cole.git Bitacora
```

**Casa:**

```bash
mkdir Boveda_Git_Casa
cd Boveda_Git_Casa
git clone https://github.com/sor-iesjj/bloque-0-curso-git.git B0_Curso_Git_Casa
git clone git@github.com:TU-USUARIO/bitacora-curso-git-casa.git Bitacora
```

Si ya habías llegado a `EJ-01-01-05`, clona además el remoto que corresponde al contexto elegido:

**Cole:**
```bash
git clone git@github.com:TU-USUARIO/manuales-boochan-cole.git Manuales
```

**Casa:**
```bash
git clone git@github.com:TU-USUARIO/manuales-boochan-casa.git Manuales
```

Si aún no has llegado a `EJ-01-01-05`, no ejecutes este clon: repite `EJ-01-01-03` a `-05` del mismo contexto para reconstruir `Manuales`. Nunca cambies a la bóveda del otro recorrido para completar este.

## 4. Comprueba cada remoto por separado

En cada carpeta clonada, ejecuta `git remote -v`. El remoto de `Bitacora` y el de `Manuales` deben incluir el mismo sufijo de contexto elegido. El remoto de `B0_Curso_Git_<contexto>` debe ser `sor-iesjj/bloque-0-curso-git` y se usa solo para leer.

> [!warning] Esta recuperación solo devuelve lo que se subió
> Las entradas y commits no publicados, así como los cambios locales, no reaparecen al clonar. La identidad global de Git y las claves SSH viven fuera de la bóveda y no se borran con ella.
