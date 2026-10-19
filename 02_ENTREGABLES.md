# Entregables del Curso de Git — Cole y Casa

> [!important] Cada práctica se graba y tiene una entrada propia
> En **cada contexto** completas 16 ejercicios, creas **16 entradas de Bitácora** y grabas la ejecución de los 16. Incluye EJ-01-01-01 y EJ-01-01-02: ahora tienen su propia entrada. Empieza por EJ-01-01-00, que comprueba Git, identidad y SSH antes de crear la bóveda.
>
> Cole y Casa son trabajos obligatorios e independientes: bóvedas fuera de SOR, repositorios, grabaciones, playlists y tareas distintos. No copies ni continúes en Casa los archivos de Cole.

## Grabación de cada práctica

1. Lee la guía y prepara su entrada antes de grabar. **Excepción inicial:** en EJ0100 la bóveda todavía no existe; usa un borrador y pásalo a Bitácora cuando el Paso 7 la cree.
2. Comprueba pantalla y micrófono en OBS. Guarda los vídeos localmente fuera de las bóvedas y repositorios: no los añadas a Git.
3. Inicia OBS antes del primer comando. Preséntate con nombre, grupo, contexto y código; muestra tu perfil de GitHub e indica qué vas a conseguir.
4. Graba el procedimiento entero mientras lo ejecutas, con explicaciones y resultados. Conserva errores, diagnóstico y corrección; no lo sustituyas por una demostración retrospectiva.
5. Anota el minuto real de cada paso. Al terminar, muestra la entrada y el resultado en GitHub, detén OBS y comprueba que el archivo se reproduce con imagen y audio.

## Plantilla de la entrada

Crea el fichero con el **nombre exacto indicado en su práctica**, dentro de `Bitacora` del contexto. Copia esta plantilla y sustituye los campos entre corchetes por tus datos y resultados reales. No copies resultados de ejemplo como si los hubieras obtenido.

```markdown
# [Código del ejercicio] — [Título] — [Cole o Casa]

## Datos del alumno
- Nombre y apellidos: [tus datos]
- Grupo: [tu grupo]
- Fecha: [fecha de realización]
- Contexto: [Cole o Casa]
- Usuario de GitHub: [tu usuario]

## Objetivo
[Qué necesitas conseguir y para qué sirve.]

## Comandos y resultados
| Comando utilizado | Qué hace | Resultado obtenido |
|---|---|---|
| [comando exacto] | [explicación propia] | [salida real o descripción comprobada] |

## Pasos y timestamps
| Paso de la práctica | Minuto en la grabación local | Minuto en el vídeo final |
|---|---|---|
| [presentación o paso] | [mm:ss real] | Pendiente de montaje |

## Errores y correcciones
| Error observado | Causa | Solución aplicada | Cómo comprobé el resultado |
|---|---|---|---|
| [error real, o indica que no hubo errores] | [causa] | [acción] | [comprobación] |

## Dudas y respuestas
[Dudas resueltas, cómo las resolviste y dudas pendientes. Si no hubo dudas, indícalo.]

## Preguntas de la práctica
[Responde con tus palabras a las preguntas del enunciado.]

## Enlaces
- Mi Bitácora en GitHub: [URL real cuando esté publicada]
- Mi repositorio Manuales: Pendiente de publicar
- Vídeo final de este contexto: Pendiente de publicar
- Timestamp de este ejercicio en el vídeo final: Pendiente de montaje
```

Antes de terminar cada ejercicio completa todos los apartados de su entrada. En EJ0100 puedes dejar los enlaces pendientes hasta que el propio procedimiento cree el remoto. **Manuales remoto todavía no existe hasta EJ-01-01-05**. El vídeo final solo existirá al cerrar la fase: entonces pega su URL en las 16 entradas y ajusta los timestamps al montaje real. Guarda y sube de nuevo las entradas que hayas completado; no basta con cambiar la copia local.

## Un vídeo final por proyecto y contexto

Cada práctica se graba durante su ejecución. Puedes hacer varias sesiones y conservar archivos locales como `EJ0100_Cole.mkv` o `EJ0100_Casa.mp4`, manteniendo la extensión real de OBS. Al completar los 16 ejercicios **reúne esas grabaciones en un único vídeo final del contexto**, en el mismo orden de las prácticas. No se pide volver a ejecutar todo ni reemplazarlo por un resumen de resultados.

- Cole: `B0.G.1.F1 · COLE · Fase 1 Fundamentos — recorrido completo`, en `B0_Curso_Git_Cole`.
- Casa: `B0.G.1.F1 · CASA · Fase 1 Fundamentos — recorrido completo`, en `B0_Curso_Git_Casa`.

En la descripción del vídeo añade `00:00 Presentación` y los timestamps **reales del montaje**: uno para el inicio de cada ejercicio y uno para cada paso dentro de él, identificados por código. Ejemplo de formato (sustituye `mm:ss`, no publiques el marcador):

```text
00:00 Presentación
mm:ss EJ0100 — Preparación y comprobaciones
mm:ss EJ0100 — Paso 1: espacio independiente
mm:ss EJ0100 — Paso 2: bóveda
[continúa con todos los pasos de EJ0100]
mm:ss EJ0101 — Comprobar Git instalado
[continúa con sus pasos y el resto de los ejercicios]
```

No incluyas contraseñas, claves privadas, frases de paso ni tokens. Si aparecen por accidente, retíralos antes de publicar sin ocultar el trabajo evaluable. Publica el vídeo como **No listado**, comprueba el enlace y añádelo a su playlist. Cole y Casa conservan cada uno su vídeo; no reutilices una grabación entre contextos.

## Qué recibe cada tarea de Teams

Cada proyecto conserva su tarea independiente y su playlist. **La tarea final lleva exactamente dos enlaces del mismo contexto**:

1. Tu repositorio de `Manuales`: `https://github.com/TU-USUARIO/manuales-boochan-cole` o `https://github.com/TU-USUARIO/manuales-boochan-casa`.
2. Su playlist `B0_Curso_Git_Cole` o `B0_Curso_Git_Casa`, con el vídeo final dentro.

El enlace directo al vídeo y su timestamp van **dentro de cada entrada de Bitácora**; no se pide un tercer enlace en la tarea. Los repositorios de Bitácora son `bitacora-curso-git-cole` y `bitacora-curso-git-casa`. Consulta [Cierre de la Fase 1](fase-1-fundamentos/Cierre_Fase_1.md) antes de entregar.

## Antes de subir una entrada

En Windows, abre Git Bash desde la carpeta `Bitacora` del contexto que vas a entregar; en macOS o Linux, abre Terminal desde esa carpeta. Antes de subir, compara la ruta completa que muestra `pwd` con la ruta de tu contexto. No ejecutes `git push` si algún componente de la ruta se llama `SOR` o `Boveda_SOR`, o si no coincide el nombre Cole/Casa.

```bash
pwd
git remote -v
git status
```

**Línea por línea:**
1. `pwd` muestra la carpeta actual. Cole debe terminar en `SOR_Git_Cole/Boveda_Git_Cole/Bitacora`; Casa, en `SOR_Git_Casa/Boveda_Git_Casa/Bitacora`. Lee también los componentes anteriores de la ruta para confirmar que no está dentro de `SOR` ni `Boveda_SOR`.
2. `git remote -v` muestra el repositorio al que se enviarían los cambios. Cole debe incluir `bitacora-curso-git-cole`; Casa debe incluir `bitacora-curso-git-casa`.
3. `git status` muestra qué cambios se prepararían o si queda algo pendiente.

Si una ruta, remoto o estado no coincide con el contexto elegido, detente: no ejecutes `git push`. Consulta al profesor y sigue [🧯 Recuperar el recorrido](03_SI_LO_ROMPES_TODO.md).

Cuando las tres comprobaciones coincidan, usa los comandos de entrega de la entrada y comprueba en GitHub que el cambio llegó al repositorio correcto. Un `push` sin error no demuestra que hayas enviado al contexto que te corresponde.

> [!warning] Repositorio de ejercicios
> Los comandos de trabajo se ejecutan en `Manuales`. Comprueba su `git remote -v`: tiene que ser `manuales-boochan-cole` en Cole y `manuales-boochan-casa` en Casa. La Bitácora se sube desde su repositorio interior. La bóveda contenedora no es un repositorio.
