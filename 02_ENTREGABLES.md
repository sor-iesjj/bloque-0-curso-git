# Entregables del Curso de Git — Cole y Casa

> **Lee esta página antes de cada recorrido.** Cole y Casa son dos trabajos independientes. Crea `SOR_Git_Cole` y `SOR_Git_Casa` fuera del árbol `SOR` y de `Boveda_SOR`; dentro va la bóveda de cada recorrido. Cada uno tiene sus repositorios, tarea y playlist, y se repite completo desde cero.

> [!danger] Una entrega por contexto
> Cole y Casa no comparten bóveda, remotos, playlist, vídeo ni tarea. Al terminar la Fase 1, entrega un único vídeo final de Cole y otro único vídeo final de Casa. No subas un vídeo independiente por ejercicio.

## Qué se conserva y qué se entrega

| Elemento | Cole | Casa |
|---|---|---|
| Entradas de Bitácora y commits | `SOR_Git_Cole/Boveda_Git_Cole/Bitacora/` → `bitacora-curso-git-cole` | `SOR_Git_Casa/Boveda_Git_Casa/Bitacora/` → `bitacora-curso-git-casa` |
| Trabajo versionado de la fase | `Manuales/` → `manuales-boochan-cole` | `Manuales/` → `manuales-boochan-casa` |
| Único vídeo de entrega de Fase 1 | Playlist `B0_Curso_Git_Cole` | Playlist `B0_Curso_Git_Casa` |
| Tarea | Tarea de Teams de Cole | Tarea de Teams de Casa |

Las entradas de Bitácora, los commits, los archivos de `Manuales` y las salidas de comandos son **evidencias de trabajo** que se conservan en sus repositorios correspondientes. No son vídeos ni entregas de Teams por cada EJ. Las comprobaciones `EJ-01-01-01` y `EJ-01-01-02` se anotan en la entrada de `EJ-01-01-00`; tampoco generan archivos de entrega separados.

## Entradas de Bitácora

Sigue el nombre exacto que da cada ejercicio. En las entradas registra qué se pedía, los comandos y su explicación, qué hiciste, el resultado, los errores y su solución, las respuestas a las preguntas y las dudas. **No añadas un enlace a un vídeo individual**: el vídeo final se enlaza en la tarea de Teams al cerrar los 16 ejercicios del contexto.

Sube cada entrada desde el repositorio `Bitacora` del contexto indicado por la guía. Antes de hacer `push`, comprueba `pwd` y `git remote -v`; nunca subas desde el contexto contrario.

## Vídeos: uno por recorrido

Al completar los 16 ejercicios de Cole, prepara y sube un único vídeo final a `B0_Curso_Git_Cole`. Repite el proceso en Casa y sube otro vídeo, distinto, a `B0_Curso_Git_Casa`. Nombre previsto:

- Cole: `B0.G.1.F1 · COLE · Fase 1 Fundamentos — recorrido completo`
- Casa: `B0.G.1.F1 · CASA · Fase 1 Fundamentos — recorrido completo`

El vídeo debe permitir reconocer al alumno y el contexto, y mostrar los resultados relevantes de los 16 códigos: `EJ-01-01-00` a `-05`, `EJ-01-02-01` a `-06` y `EJ-01-03-01` a `-04`. No hace falta volver a teclear cada comando; muestra los productos, estados e historiales resultantes en la bóveda y en GitHub, explicando brevemente qué demuestra cada uno. Organiza la descripción con capítulos/timestamps para los 16 códigos, además de la presentación.

Las capturas de pantalla, la Bitácora y los commits son evidencias intermedias y permanecen en los repositorios del contexto. No se suben como clips separados. Publica el vídeo final dentro de la playlist del contexto. En la descripción de cada tarea de Teams incluye **exactamente dos enlaces del mismo contexto** —el repositorio de Manuales y la playlist, donde estará el vídeo—; no añadas un tercer enlace al vídeo:

1. Repositorio de `Manuales`: `https://github.com/TU-USUARIO/manuales-boochan-cole` o `https://github.com/TU-USUARIO/manuales-boochan-casa`.
2. Playlist correspondiente: enlace de `B0_Curso_Git_Cole` o `B0_Curso_Git_Casa`.

No pongas en la tarea enlaces del otro contexto ni del repositorio público del profesor. La secuencia de grabación y cierre está detallada en [Cierre de la Fase 1](fase-1-fundamentos/Cierre_Fase_1.md).

## Antes de subir una entrada

Abre una terminal dentro de `Bitacora` del espacio independiente correspondiente y verifica primero que la ruta física no tiene ningún ancestro llamado `SOR` o `Boveda_SOR`. Si aparece, no ejecutes nada y sigue la guía de recuperación.

```bash
pwd -P
ruta=$(pwd -P | tr '[:upper:]' '[:lower:]')
case "$ruta" in
  */sor|*/sor/*|*/boveda_sor|*/boveda_sor/*) echo "ERROR: ubicación dentro de SOR; detente"; exit 1 ;;
  */sor_git_cole/boveda_git_cole/bitacora|*/sor_git_casa/boveda_git_casa/bitacora) echo "Ruta fuera de SOR" ;;
  *) echo "ERROR: ruta/contexto incorrectos; detente"; exit 1 ;;
esac
git remote -v
git status
```

Para Cole, `pwd` debe terminar en `SOR_Git_Cole/Boveda_Git_Cole/Bitacora` y el remoto incluir `bitacora-curso-git-cole`. Para Casa, debe terminar en `SOR_Git_Casa/Boveda_Git_Casa/Bitacora` y nombrar `bitacora-curso-git-casa`. Si algo difiere, detente y no ejecutes `git push`.

Después, usa los comandos de entrega de la entrada y comprueba en GitHub que aparece en el repositorio correcto. Un `push` sin error no demuestra que hayas enviado al contexto que te corresponde.

> [!warning] Repositorio de ejercicios
> Los comandos de trabajo se ejecutan en `Manuales`. Comprueba su `git remote -v`: tiene que ser `manuales-boochan-cole` en Cole y `manuales-boochan-casa` en Casa. La Bitácora se sube desde su repositorio interior. La bóveda contenedora no es un repositorio.
