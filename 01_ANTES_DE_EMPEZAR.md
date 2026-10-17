# Antes de empezar — dos recorridos independientes

> **Módulo:** SOR · Bloque 0 · Curso de Git
> **Cuándo se lee:** antes de iniciar cada recorrido.

> [!danger] Cole y Casa se hacen dos veces, desde cero
> Completa el recorrido **Cole** en el equipo del centro y el recorrido **Casa** en tu equipo de casa. No continúes trabajo entre equipos, no clones el repositorio de Cole para seguir en Casa y no reutilices la bóveda ni los repositorios personales. Cada recorrido tiene sus propios nombres y su propia entrega. En cada equipo crea un espacio neutral `SOR_Git_Cole` o `SOR_Git_Casa` en Documentos local, fuera del árbol `SOR` y de `Boveda_SOR`; no copies el trabajo de Cole.

## Estructura que crearás en cada contexto

| Uso | Cole | Casa | Relación con GitHub |
|---|---|---|---|
| Espacio y bóveda contenedora | `SOR_Git_Cole/Boveda_Git_Cole` | `SOR_Git_Casa/Boveda_Git_Casa` | Fuera de SOR; no es un repositorio |
| Enunciados del profesor | `B0_Curso_Git_Cole` | `B0_Curso_Git_Casa` | Copias separadas del mismo repo público, solo lectura |
| Apuntes y entregas | `Bitacora` | `Bitacora` | Remotos `bitacora-curso-git-cole` / `bitacora-curso-git-casa` |
| Ejercicios | `Manuales` | `Manuales` | Remotos `manuales-boochan-cole` / `manuales-boochan-casa` |
| Playlist del vídeo final | `B0_Curso_Git_Cole` | `B0_Curso_Git_Casa` | Un solo vídeo al cerrar Fase 1 y una tarea por contexto |

Los nombres interiores pueden coincidir porque cada recorrido vive en un espacio distinto. Los espacios `SOR_Git_Cole` y `SOR_Git_Casa` se crean fuera del árbol `SOR`; comprueba cada ruta física antes de ejecutar comandos. Si cualquier ancestro de la ruta se llama exactamente `SOR` o `Boveda_SOR`, detente. No basta con comprobar el sufijo de la ruta. En GitHub los repositorios personales sí llevan sufijo `-cole` o `-casa`; comprueba el remoto antes de cada `push`. Los repositorios de apoyo del profesor siguen siendo compartidos y se clonan solo cuando el ejercicio lo indique.

## Orden obligatorio

1. En el contexto que vas a trabajar, completa [`EJ-01-01-01`](fase-1-fundamentos/EJ-01-01-01.md) y [`EJ-01-01-02`](fase-1-fundamentos/EJ-01-01-02.md). Si Git no está instalado en ese equipo, instálalo con la guía; consulta la identidad global sin cambiarla.
2. Sigue la edición correspondiente de [`EJ-01-01-00`](fase-1-fundamentos/EJ-01-01-00.md). Allí crearás el espacio y la bóveda fuera del árbol SOR, la bitácora y clonarás el material público del profesor para leerlo.
3. Para los ejercicios siguientes, abre siempre la carpeta del mismo contexto: Cole o Casa. Completa la secuencia `-03` → `-04` → `-05` en ese mismo recorrido.

> [!warning] GitHub del profesor y repositorios personales
> `sor-iesjj/bloque-0-curso-git` es material común de lectura. Tus repositorios personales son otros: `bitacora-curso-git-cole` y `manuales-boochan-cole` para Cole; `bitacora-curso-git-casa` y `manuales-boochan-casa` para Casa. No subas trabajo al repositorio del profesor ni uses el remoto de un contexto en el otro.

La Fase 1 completa se irá adaptando por tramos. Las ediciones Cole/Casa vigentes de este tramo son únicamente las que el índice declara disponibles. Las Fases 2–5 conservan material anterior que presupone la ubicación vieja; están **no disponibles para ejecución** hasta que tengan guías actualizadas con espacios independientes. No ejecutes ni entregues esas guías comunes.
