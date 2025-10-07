# Universidad [Nombre de la Universidad]  
## Facultad de [Nombre de la Facultad]  
### Carrera de Ingeniería en Software  

**Asignatura:** Manejo y Configuración de Software  
**Nombre del Estudiante:** Evelyn Cardenas  
**Fecha:** 07/10/2025  

---

# Evaluación Práctica de Git y GitHub

## Instrucciones Generales

- Cada pregunta debe ser respondida directamente en este archivo **(README.md)** debajo del enunciado correspondiente.
- Cada respuesta debe ir acompañada de uno o más **commits**, según se indique en cada pregunta.
- Cuando se indique, deberán realizarse acciones prácticas dentro del repositorio (como creación de archivos, ramas, resolución de conflictos, etc.).
- Cada pregunta debe estar **etiquetada con un tag**, únicamente en el commit final correspondiente, con el formato: `"Pregunta 1"`, `"Pregunta 2"`, etc.

---

## Pregunta 1 (1 punto)

**Explicar la diferencia entre los siguientes conceptos/comandos en Git y GitHub:**

- `git clone`  
- `fork`  
- `git pull`

### Parte práctica:

- Realizar un **fork** de este repositorio en la cuenta personal de GitHub del estudiante.
- Luego, realizar un **clone** del fork en el equipo local.
- En este README, describir el proceso seguido:
  - ¿Cómo se realizó el fork?
  - ¿Cómo se realizó el clone del fork?
  - ¿Cómo se verificó que se estaba trabajando sobre el fork y no sobre el repositorio original?

**📝 Respuesta:**

- Parte teórica:

La diferencia entre los tres comandos en Git se basa en.:

  - git clone: copia un repositorio remoto (historial completo) a tu equipo y configura el remoto origin.
  - Fork: copia en tu cuenta de GitHub el repositorio de otra persona (crea tu propio remoto). Sirve para proponer cambios sin permisos directos sobre el repo original.
  - git pull: trae commits del remoto y los integra en tu rama actual (equivalente a fetch + merge o fetch + rebase según config).

- Parte práctica:  

- Parte práctica:

### ¿Cómo se realizó el fork?

El fork se realizó directamente desde la página del repositorio original en GitHub.  
En la parte superior derecha de la página, se hizo clic en el botón Fork y se seleccionó mi cuenta personal.  
Esto creó una copia exacta del repositorio en mi perfil de GitHub, donde puedo trabajar de forma independiente sin afectar el proyecto original.


---

### ¿Cómo se realizó el clone del fork?

Una vez creado el fork, se copió la URL del nuevo repositorio (ubicado en mi cuenta) usando el botón Code → HTTPS.  
Luego, desde Git Bash, se ejecutó el siguiente comando para clonar el fork en mi equipo local:

![alt text](<Captura de pantalla 2025-10-07 151835.png>)

---

### ¿Cómo se verificó que se estaba trabajando sobre el fork y no sobre el repositorio original?

Se verifico que el repositorio local apuntaba al fork personal y no al original con ayuda del comando git remote -v:

![alt text](<Captura de pantalla 2025-10-07 152500.png>)

---

## Pregunta 2 (1 punto)

**Configurar un archivo `.gitignore` para que ignore:**

- Todos los archivos con extensión `.log`.
- Una carpeta llamada `temp/`.
- Todos los archivos `.md` y `.txt`de la carpeta `doc/`. (Probar agregando un archivo `prueba.md` y un archivo `prueba.txt` dentro de la carpeta y fuera de la carpeta.)

### Requisitos:

1. Realizar un **primer commit** que incluya únicamente el archivo `.gitignore` con las reglas de exclusión definidas.
2. Realizar un **segundo commit** donde se explique en este README la función del archivo `.gitignore` y se muestre evidencia de que los archivos y carpetas indicadas no están siendo rastreadas por Git.

**Importante:**  
- Solo el **segundo commit** debe llevar el **tag `"Pregunta 2"`**.

**📝 Respuesta:**

<!-- Escribe aquí tu explicación y evidencia para la Pregunta 2 -->

### Reglas usadas en `.gitignore`

- `*.log` → ignora todos los archivos de bitácora.
- `temp/` → ignora la carpeta `temp` completa.
- `doc/*.md` y `doc/*.txt` → ignora solo los `.md` y `.txt que estén dentro de `doc/`.
  > Nota: Los archivos `.md` y `.txt` **fuera** de `doc/` no se ignoran.

![alt text](image.png)

### Evidencia de funcionamiento

1. Archivos de prueba:
   - **Dentro de `doc/`**: `doc/prueba.md`, `doc/prueba.txt` → **ignorados**.
   - **Fuera de `doc/`**: `prueba.md`, `prueba.txt` → **NO ignorados** (Git los muestra como *untracked*).
   - `app.log` (en la raíz) → **ignorado**.
   - Carpeta `temp/` → **ignorada**.

   ![alt text](image-1.png)

2. Comandos ejecutados:

Ver todo lo ignorado de forma resumida:
git status --ignored -s

Ver por qué un archivo está ignorado (muestra la regla que coincide):
git check-ignore -v doc/prueba.md doc/prueba.txt app.log

---

## Pregunta 3 (2 puntos)

**Utilizar Git Flow para desarrollar una nueva funcionalidad llamada `ingresar-encabezado`.**

### Requisitos:

- Inicializar el repositorio con Git Flow, utilizando las ramas por defecto: `main` y `develop`.
- Crear una rama de tipo `hotfix` con el nombre `ingresar-encabezado`.
- En dicha rama, **completar con los datos personales del estudiante** el encabezado que ya se encuentra al inicio de este archivo `README.md`.
- Realizar al menos un commit durante el desarrollo.
- Finalizar el hotfix siguiendo el flujo de trabajo establecido por Git Flow.

### En este README, se debe incluir:

- Los **comandos exactos** utilizados desde la inicialización de Git Flow hasta el cierre del hotfix.
- Una descripción del **proceso seguido**, indicando el propósito de cada paso.
- Una reflexión sobre las **ventajas de aplicar Git Flow**, especialmente en contextos colaborativos o proyectos de larga duración.

**Importante:**

- Deben realizarse varios commits durante esta pregunta.
- **Solo el commit final** debe llevar el **tag `"Pregunta 3"`**.
- El flujo debe respetar la estructura de Git Flow con las ramas `develop` y `main`.

**📝 Respuesta:**

### Comandos exactos utilizados (Git Flow)

# Inicializar Git Flow con ramas por defecto (main / develop)
git flow init -d

# Crear hotfix para la tarea solicitada
git flow hotfix start ingresar-encabezado

# (Editar README: completar encabezado con mis datos)
git add README.md
git commit -m "Q3: Añade datos personales al encabezado (avance 1)"

# (Opcional: más commits si hubo cambios adicionales)
# git commit -m "Q3: Ajusta formato del encabezado"

# Finalizar el hotfix (merges a main y develop + tag de versión de Git Flow)
git flow hotfix finish -m "Q3: Cierra hotfix ingresar-encabezado" ingresar-encabezado

# Publicar ramas y tags
git push origin main
git push origin develop
git push origin --tags

# Tag requerido por el examen (solo en el commit final)
git checkout develop
git tag -a "Pregunta 3" -m "Pregunta 3"
git push origin --tags

---
Proceso seguido (propósito de cada paso)

git flow init -d: configura la estrategia Git Flow con main (producción) y develop (integración).

![alt text](image-2.png)

git flow hotfix start ingresar-encabezado: crea una rama hotfix desde main para aplicar un cambio urgente (completar el encabezado del README).

![alt text](image-3.png)

Commits en el hotfix: guardan el progreso de la edición del encabezado con mis datos personales.

git flow hotfix finish ...: cierra el hotfix; fusiona automáticamente a main y replica a develop, además crea un tag de versión propio de Git Flow.

Push de ramas/tags: publica main, develop y los tags en el remoto.

Tag “Pregunta 3”: etiqueta del examen aplicada solo al commit final (se coloca en develop tras finalizar el hotfix).
---
Reflexión: ventajas de aplicar Git Flow

Orden y roles claros de ramas: feature, release, hotfix, develop, main. Reduce errores al separar trabajo en progreso de producción.

Soporte para parches urgentes: un hotfix permite corregir rápido en main sin bloquear el desarrollo en develop.

Escala en equipos grandes/proyectos largos: facilita revisiones, releases predecibles y auditoría del historial (tags por versión y ramas temáticas).
---

## Pregunta 4 (2 puntos)

**Trabajo con Issues y Pull Requests**

### Parte teórica:

- Explicar qué es un **issue** en GitHub.
- Explicar qué es un **pull request** y cuál es su finalidad.
- Indicar la diferencia entre ambos y cómo se relacionan en un entorno de trabajo colaborativo.

### Parte práctica:

- Trabajar en la rama `develop`, ya existente desde la configuración de Git Flow.
- Crear un **issue** titulado `"Respuesta a la Pregunta 4"`, en el que se indique que su objetivo es documentar esta pregunta.
- Realizar los cambios necesarios en este archivo `README.md` para responder esta pregunta.
- Realizar un **commit** con los cambios y subirlo a la rama `develop` del repositorio remoto.
- Crear un **pull request** desde `develop` hacia `main` en GitHub.
- **Vincular el pull request con el issue creado**, de manera que al ser aprobado y fusionado, el issue se cierre automáticamente.
- **Aprobar** el pull request para que se haga el merge respectivo hacia `main`.

### En este README, se debe incluir:

- Un resumen del procedimiento realizado.
- El número y enlace del issue creado.
- El número y enlace al pull request.

**📝 Respuesta:**

<!-- Escribe aquí tu respuesta completa a la Pregunta 4 -->

---

## Pregunta 5 (2 puntos)

**Resolver conflictos entre ramas y realizar un Pull Request**

### Requisitos:

- Crear dos ramas llamadas `ramaA` y `ramaB`, ambas a partir de la rama `develop`.
- En `ramaA`, crear un archivo llamado `archivoA.txt` con el contenido:  
  `Contenido A`
- En `ramaB`, crear un archivo con el mismo nombre (`archivoA.txt`), pero con el contenido:  
  `Contenido B`
- Intentar fusionar `ramaB` sobre `ramaA`, lo cual debe generar un conflicto.
- Resolver el conflicto combinando ambos contenidos.
- Realizar el merge de `ramaA` hacia `develop`.
- Crear un **pull request** desde `develop` hacia `main`.
- Una vez completado lo anterior, eliminar las ramas `ramaA` y `ramaB` tanto local como remotamente.

### En este README, se debe incluir:

- El procedimiento completo:
  - Cómo se crearon las ramas.
  - Cómo se generó y resolvió el conflicto.
  - Cómo se realizó el merge hacia `develop`.
  - Cómo se eliminaron las ramas al finalizar.
- El enlace al pull request.
- Una breve explicación de qué es un conflicto en Git y por qué ocurrió en este caso.

**📝 Respuesta:**

<!-- Escribe aquí tu respuesta completa a la Pregunta 5 -->

---

## Pregunta 6 (2 puntos)

**Realizar limpieza, explicar versionamiento semántico y enviar cambios al repositorio original**

### Requisitos:

- Trabajar en la rama `develop` del fork del repositorio.
- Eliminar los archivos `archivoA.txt` y `archivoB.txt` creados en preguntas anteriores.
- Realizar un merge desde `develop` hacia `main` en el repositorio local.
- Enviar los cambios de la rama `main` local a la rama `develop` del repositorio remoto (fork). Recuerde incluir todos los tags creados (6 tags).
- Finalmente, crear un **pull request** desde la rama `develop` del fork hacia la rama `main` del repositorio original (del cual se realizó el fork en la Pregunta 1). El titulo del pull request debe ser "NOMBRE APELLIDOS", en la descripción colocar el link de su repositorio de GitHub.

### En este README, se debe incluir:

- Una explicación del proceso realizado paso a paso.
- Una explicación del **versionamiento semántico**, indicando:
  - En qué consiste.
  - Sus tres componentes (MAJOR, MINOR, PATCH).
- El enlace al pull request creado hacia el repositorio original.
- Si hace falta agregar alguna evidencia adicional, agregue un tag adicional que sea `Version Final`.

**📝 Respuesta:**

<!-- Escribe aquí tu respuesta completa a la Pregunta 6 -->
