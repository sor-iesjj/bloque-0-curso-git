# Recuperar el recorrido de Git — Cole o Casa

> Usa esta guía si el espacio de Git está en la ubicación equivocada o el repositorio no se puede reparar con seguridad. Recupera un contexto cada vez y conserva cualquier carpeta existente.

> [!danger] No borres ni muevas la bóveda real
> El trabajo de Git debe vivir fuera del árbol `SOR` y de `Boveda_SOR`. **No uses `rm -rf`, no uses `rmdir`, no vacíes la papelera y no muevas ni renombres `SOR` o `Boveda_SOR`.** La recuperación se hace con el Explorador/Finder en una ubicación neutral y conserva cualquier trabajo fuera de SOR. No selecciones nada dentro del árbol SOR; si el curso ya se creó allí, detente y pregunta al profesor.

## 1 · Elige un solo contexto y comprueba la ubicación

| Recorrido | Espacio independiente | Bóveda del curso | Bitácora remota | Manuales remoto |
|---|---|---|---|---|
| Cole | `SOR_Git_Cole` | `Boveda_Git_Cole` | `bitacora-curso-git-cole` | `manuales-boochan-cole` |
| Casa | `SOR_Git_Casa` | `Boveda_Git_Casa` | `bitacora-curso-git-casa` | `manuales-boochan-casa` |

Cierra Obsidian y las terminales que estén abiertas en el curso. En el Explorador/Finder, localiza la carpeta del contexto elegido. Su ubicación correcta es `Documentos local/SOR_Git_<contexto>/Boveda_Git_<contexto>`, o una carpeta local equivalente fuera de OneDrive. El espacio `SOR_Git_<contexto>` debe estar fuera del árbol `SOR`; no basta con que el nombre de la bóveda coincida.

> [!danger] Si la carpeta está dentro de `Boveda_SOR`
> No la renombres, muevas ni abras. No ejecutes comandos desde esa ruta. Deja el contenido intacto y contacta con el profesor para que te ayude a identificarlo sin arriesgar tus apuntes reales.

Si el espacio `SOR_Git_<contexto>` o la bóveda del curso aparecen dentro de `SOR`, **déjalos exactamente como están**: no abras, renombres, muevas ni borres nada de ese árbol. Contacta con el profesor para que valore cómo conservarlo sin tocar tus apuntes reales. Después, inicia un laboratorio limpio en el espacio independiente correspondiente, creado fuera de `SOR`.

## 2 · Crea un espacio neutral nuevo

En Documentos local, crea `SOR_Git_Cole` o `SOR_Git_Casa` al mismo nivel que `SOR` si esta existe; nunca dentro de ella. Si Documentos se sincroniza con OneDrive, elige una carpeta local fuera de OneDrive. No selecciones ni abras `SOR` o `Boveda_SOR`. Dentro del espacio nuevo, abre Git Bash/Terminal y comprueba la ruta antes de crear nada:

```bash
pwd -P
ruta=$(pwd -P | tr '[:upper:]' '[:lower:]')
case "$ruta" in
  */sor|*/sor/*|*/boveda_sor|*/boveda_sor/*) echo "ERROR: ubicación dentro de SOR; detente"; exit 1 ;;
  */sor_git_cole|*/sor_git_casa) echo "Espacio neutral" ;;
  *) echo "ERROR: ubicación no reconocida; detente"; exit 1 ;;
esac
if git rev-parse --show-toplevel >/dev/null 2>&1; then echo "ERROR: ya heredas un repositorio Git; detente"; exit 1; fi
```

Línea 1 muestra la ruta física. `tr` normaliza mayúsculas/minúsculas, `case` detiene el proceso si algún componente de la ruta es exactamente `SOR` o `Boveda_SOR`, y `git rev-parse` comprueba que no heredas un repositorio Git; continúa solo desde uno de los espacios `SOR_Git_*`. Si no aparece `Espacio neutral`, cierra la terminal y corrige la ubicación desde el Explorador/Finder.

## 3 · Recrea la bóveda en el espacio elegido

Ejecuta solo el bloque del contexto elegido, desde el directorio neutral comprobado. Sustituye `TU-USUARIO` por tu usuario real de GitHub.

**Cole:**
```bash
ruta=$(pwd -P | tr '[:upper:]' '[:lower:]')
case "$ruta" in
  */sor|*/sor/*|*/boveda_sor|*/boveda_sor/*) echo "ERROR: ubicación dentro de SOR; detente"; exit 1 ;;
  */sor_git_cole) echo "Espacio Cole correcto" ;;
  *) echo "ERROR: no estás en SOR_Git_Cole; detente"; exit 1 ;;
esac
if git rev-parse --show-toplevel >/dev/null 2>&1; then echo "ERROR: ya heredas un repositorio Git; detente"; exit 1; fi
mkdir Boveda_Git_Cole
cd Boveda_Git_Cole
pwd -P
ruta=$(pwd -P | tr '[:upper:]' '[:lower:]')
case "$ruta" in
  */sor|*/sor/*|*/boveda_sor|*/boveda_sor/*) echo "ERROR: ubicación dentro de SOR; detente"; exit 1 ;;
  */sor_git_cole/boveda_git_cole) echo "Ruta Cole correcta" ;;
  *) echo "ERROR: ruta distinta; detente"; exit 1 ;;
esac
if git rev-parse --show-toplevel >/dev/null 2>&1; then echo "ERROR: ya heredas un repositorio Git; detente"; exit 1; fi
git clone https://github.com/sor-iesjj/bloque-0-curso-git.git B0_Curso_Git_Cole
git clone git@github.com:TU-USUARIO/bitacora-curso-git-cole.git Bitacora
```

**Casa:**
```bash
ruta=$(pwd -P | tr '[:upper:]' '[:lower:]')
case "$ruta" in
  */sor|*/sor/*|*/boveda_sor|*/boveda_sor/*) echo "ERROR: ubicación dentro de SOR; detente"; exit 1 ;;
  */sor_git_casa) echo "Espacio Casa correcto" ;;
  *) echo "ERROR: no estás en SOR_Git_Casa; detente"; exit 1 ;;
esac
if git rev-parse --show-toplevel >/dev/null 2>&1; then echo "ERROR: ya heredas un repositorio Git; detente"; exit 1; fi
mkdir Boveda_Git_Casa
cd Boveda_Git_Casa
pwd -P
ruta=$(pwd -P | tr '[:upper:]' '[:lower:]')
case "$ruta" in
  */sor|*/sor/*|*/boveda_sor|*/boveda_sor/*) echo "ERROR: ubicación dentro de SOR; detente"; exit 1 ;;
  */sor_git_casa/boveda_git_casa) echo "Ruta Casa correcta" ;;
  *) echo "ERROR: ruta distinta; detente"; exit 1 ;;
esac
if git rev-parse --show-toplevel >/dev/null 2>&1; then echo "ERROR: ya heredas un repositorio Git; detente"; exit 1; fi
git clone https://github.com/sor-iesjj/bloque-0-curso-git.git B0_Curso_Git_Casa
git clone git@github.com:TU-USUARIO/bitacora-curso-git-casa.git Bitacora
```

No sigas con los `git clone` si la comprobación no muestra la ruta correcta. Si habías llegado a `EJ-01-01-05`, clona también el repositorio `Manuales` del mismo contexto:

**Cole:**
```bash
git clone git@github.com:TU-USUARIO/manuales-boochan-cole.git Manuales
```

**Casa:**
```bash
git clone git@github.com:TU-USUARIO/manuales-boochan-casa.git Manuales
```

Si todavía no habías llegado a `EJ-01-01-05`, no ejecutes ese clon: continúa `EJ-01-01-03` a `-05` en el mismo contexto. Nunca uses un remoto del otro recorrido.

## 4 · Comprueba los remotos

En `Bitacora` y, si existe, `Manuales`, confirma por separado `pwd` y `git remote -v`. La ruta debe estar bajo el espacio neutral correcto y cada remoto debe llevar el sufijo de contexto elegido. `B0_Curso_Git_<contexto>` debe apuntar a `sor-iesjj/bloque-0-curso-git` y es solo de lectura. Si una ruta contiene `/SOR/` o `/Boveda_SOR/`, cierra la terminal sin ejecutar más comandos.

> [!warning] La recuperación solo reconstruye lo que llegó a GitHub
> Una entrada o commit sin publicar no aparece al clonar. Conserva la carpeta renombrada `-RESERVA`; antes de recuperar datos locales, pide ayuda al profesor. La identidad global de Git y las claves SSH viven fuera de estas carpetas y no se eliminan con esta recuperación.
