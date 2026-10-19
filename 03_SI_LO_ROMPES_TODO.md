# Recuperar el recorrido de Git — Cole o Casa

> Usa esta guía si crees que creaste el espacio en una ubicación incorrecta, no sabes en qué carpeta estás o no puedes continuar con seguridad. Recupera un contexto cada vez.

> [!danger] Protege tus apuntes reales
> El laboratorio del curso debe estar fuera de la carpeta `SOR` y de la bóveda real `Boveda_SOR`. Si cualquier parte del curso aparece dentro de `SOR` o `Boveda_SOR`, **no la abras, no la muevas, no la renombres y no la borres**. Cierra la terminal y pide ayuda al profesor. No uses comandos de borrado ni vacíes la papelera.

## 1 · Detente y conserva lo que existe

Cierra Obsidian y las terminales abiertas en el laboratorio. No intentes arreglar una ruta moviendo carpetas a ciegas. Si ya existe `SOR_Git_Cole`, `SOR_Git_Casa`, `Boveda_Git_Cole` o `Boveda_Git_Casa`, déjalo tal como está hasta que el profesor confirme qué contiene y dónde debe quedar.

Cole y Casa son laboratorios separados:

| Recorrido | Espacio | Bóveda | Bitácora | Manuales |
|---|---|---|---|---|
| Cole | `SOR_Git_Cole` | `Boveda_Git_Cole` | `bitacora-curso-git-cole` | `manuales-boochan-cole` |
| Casa | `SOR_Git_Casa` | `Boveda_Git_Casa` | `bitacora-curso-git-casa` | `manuales-boochan-casa` |

## 2 · Pide ayuda si hay material que proteger

Si el espacio está dentro de `SOR`/`Boveda_SOR`, si no reconoces las carpetas o si hay cambios que no llegaron a GitHub, detente y consulta al profesor. No intentes recuperar por tu cuenta: una carpeta local puede contener trabajo que no esté publicado.

El profesor decidirá cómo conservar ese material. La recuperación no implica cambiar ni reorganizar tus apuntes reales.

## 3 · Empieza un laboratorio limpio, solo después de confirmarlo

Cuando el profesor te indique una ubicación nueva, créala desde el Explorador/Finder en una carpeta local fuera de `SOR` y de `Boveda_SOR`. Puede estar fuera de OneDrive; no hace falta colocarla al mismo nivel que `SOR`. El árbol hermano que aparece en algunos ejemplos es solo una posibilidad.

Después, sigue desde el principio `EJ-01-01-00` del contexto elegido: Cole o Casa. Abre Git Bash desde la carpeta recién creada cuando lo indique la guía y compara la salida de `pwd` con la ruta Cole/Casa antes de clonar o inicializar cualquier repositorio. Si la ruta no coincide o tienes dudas, detente y pregunta al profesor.

No reutilices carpetas existentes ni remotos del otro contexto. El repositorio del curso es de solo lectura; los repositorios de Bitácora y Manuales deben llevar el sufijo del contexto elegido.
