# Universidad Tecnica de Ambato 
## Facultad de Ingenieria en Sistemas electronica e Industrial.  
### Carrera de Ingeniería en Software  

**Asignatura:** Manejo y Configuración de Software  
**Nombre del Estudiante:** Carlos Giovanni Ramos Jacome
**Fecha:** 30 de Marzo del 2025 

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

Diferencias entre git clone, fork y pull
git clone
Crea una copia local de un repositorio remoto.  

fork
Copia de un repositorio en tu cuenta de GitHub para trabajar independientemente.

git pull
Descarga y fusiona los cambios realizados del repositorio remoto a mi repositorio local.

Evidencias del clone 
![Logo](img1.jpeg)

Como se realizo el fork :
  Fui al repositorio dado por el ingeniero 
  En la parte superior derecha hay un boton llamado Fork al hacer click sobre el me lleva aun apartado en donde se me indica al reposiotrio destion en este caso seria mi repositorio local y finalmente se crea el fork.

Como se realizo el clone del frok:
  Desde mi repositorio local, en el boton code se copia el link para clonar mi repositorio, y creo una carpeta para lonar este repositorio, utilizo el comando git clone mas el link de mi repositorio y se clono.

Cómo se verificó que se estaba trabajando sobre el fork y no sobre el repositorio original:
  Ejecutando el comando git remote -v que me indica que estoy trabajando sobre min repositorio local y no sobre el original.
  Evidencias:
  ![Logo](img2.jpeg)
---

## Pregunta 2 (1 punto)

**Configurar un archivo `.gitignore` para que ignore:**

- Todos los archivos con extensión `.log`.
- Una carpeta llamada `temp/`.

### Requisitos:

1. Realizar un **primer commit** que incluya únicamente el archivo `.gitignore` con las reglas de exclusión definidas.
2. Realizar un **segundo commit** donde se explique en este README la función del archivo `.gitignore` y se muestre evidencia de que los archivos y carpetas indicadas no están siendo rastreadas por Git.

**Importante:**  
- Solo el **segundo commit** debe llevar el **tag `"Pregunta 2"`**.

**📝 Respuesta:**

El archivo `.gitignore` es utilizado por Git para especificar qué archivos o directorios deben ser ignorados. En este caso, el archivo `.gitignore` está configurado para ignorar:
- Todos los archivos con extensión `.log`.
- La carpeta `temp/`.

Para vefrificar que se estan ignorando se ejecuta git status y se evidencia lo siguiente
  ![Logo](img3.jpeg)

---

## Pregunta 3 (2 puntos)

**Utilizar Git Flow para desarrollar una nueva funcionalidad llamada `ingresar-encabezado`.**

### Requisitos:

- Inicializar el repositorio con Git Flow, utilizando las ramas por defecto: `main` y `develop`.
- Crear una rama de tipo `feature` con el nombre `ingresar-encabezado`.
- En dicha rama, **completar con los datos personales del estudiante** el encabezado que ya se encuentra al inicio de este archivo `README.md`.
- Realizar al menos un commit durante el desarrollo.
- Finalizar la feature siguiendo el flujo de trabajo establecido por Git Flow.

### En este README, se debe incluir:

- Los **comandos exactos** utilizados desde la inicialización de Git Flow hasta el cierre de la feature.
- Una descripción del **proceso seguido**, indicando el propósito de cada paso.
- Una reflexión sobre las **ventajas de aplicar Git Flow**, especialmente en contextos colaborativos o proyectos de larga duración.

**Importante:**

- Deben realizarse varios commits durante esta pregunta.
- **Solo el commit final** debe llevar el **tag `"Pregunta 3"`**.
- El flujo debe respetar la estructura de Git Flow con las ramas `develop` y `main`.

**📝 Respuesta:**

Pasos ycomandos usados desde la inicializacion:

git flow init

Crear y comenzar la rama feature/ingresar-encabezado:
git flow feature start ingresar-encabezado

Modificamos el encabezado

Finalizar la funcionalidad de la feature:
git flow feature finish ingresar-encabezado

Subir cambios a GitHub:
git push origin develop

Descripcion:

Inicializamos Git Flow con git flow init, creando las ramas main y develop.

Creamos la rama de la feature con git flow feature start ingresar-encabezado y trabajamos en el archivo README.md para completar los datos personales del estudiante.

Finalizamos la rama de la feature con git flow feature finish ingresar-encabezado, fusionando los cambios en develop.

Finalmente, subimos los cambios al repositorio remoto.

Ventajas de gitflow
Git Flow ofrece una estructura organizada para el desarrollo de software, ideal para proyectos colaborativos o de larga duración. Permite trabajar en funcionalidades de manera independiente sin afectar el trabajo de otros, lo que facilita la colaboración. Además, facilita la creación de versiones estables y la corrección de errores de manera controlada, mejorando la calidad y gestión del código.
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
- Crear un **pull request** desde `develop` hacia `develop` en GitHub.
- **Vincular el pull request con el issue creado**, de manera que al ser aprobado y fusionado, el issue se cierre automáticamente.
- El repositorio debe estar **configurado para requerir una revisión previa al merge**, la cual **debe ser aprobada por el docente**.

### En este README, se debe incluir:

- Un resumen del procedimiento realizado.
- El número del issue creado.
- El enlace al pull request.
- Una explicación de cómo se comprobó que el repositorio requería revisión antes de aceptar el pull request (por ejemplo, a través del mensaje mostrado por GitHub).

**📝 Respuesta:**

<!-- Escribe aquí tu respuesta completa a la Pregunta 4 -->

Un issue en GitHub es una herramienta para realizar un seguimiento de tareas, errores o solicitudes de mejora en un proyecto. Permite a los colaboradores comunicar problemas o sugerir cambios.
Un pull request es una solicitud para fusionar los cambios realizados en una rama de un repositorio con otra rama, generalmente de un repositorio principal. Su finalidad es permitir la revisión y discusión antes de integrar los cambios.

Diferencia 
Issue: Es un seguimiento de tareas o problemas. Sirve para identificar lo que debe hacerse o corregirse en el proyecto.

Pull request: Es una solicitud para integrar cambios al código, y se crea generalmente como resultado de resolver un issue.

Para colaborar en un proyecto utilizando GitHub, seguimos estos pasos:

1. Crear **issues** para tareas, errores o características a implementar.
2. Trabajar en ramas para desarrollar funcionalidades.
3. Crear **pull requests** para revisar y fusionar los cambios.
4. Hacer **revisiones de código** para garantizar calidad y evitar errores.

Estos pasos facilitan la colaboración en proyectos de equipo.
---

## Pregunta 5 (2 puntos)

**Resolver conflictos entre ramas y realizar un Pull Request controlado**

### Requisitos:

- Crear dos ramas llamadas `ramaA` y `ramaB`, ambas a partir de la rama `main`.
- En `ramaA`, crear un archivo llamado `archivoA.txt` con el contenido:  
  `Contenido A`
- En `ramaB`, crear un archivo con el mismo nombre (`archivoA.txt`), pero con el contenido:  
  `Contenido B`
- Intentar fusionar `ramaB` sobre `ramaA`, lo cual debe generar un conflicto.
- Resolver el conflicto combinando ambos contenidos (por ejemplo: `Contenido combinado A+B`).
- Realizar el merge de `ramaA` hacia `develop`.
- Crear un **pull request** desde `ramaA` hacia `develop`.
- El pull request debe estar **configurado para requerir revisión y ser aprobado por el docente**.
- Una vez completado el merge, eliminar las ramas `ramaA` y `ramaB` tanto local como remotamente.

### En este README, se debe incluir:

- El procedimiento completo:
  - Cómo se crearon las ramas.
  - Cómo se generó y resolvió el conflicto.
  - Cómo se realizó el merge hacia `develop`.
  - Cómo se creó y vinculó el pull request.
  - Cómo se verificó que la revisión fue requerida y aprobada.
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
- Enviar los cambios de la rama `main` local a la rama `develop` del repositorio remoto (fork).
- Finalmente, crear un **pull request** desde la rama `develop` del fork hacia la rama `main` del repositorio original (del cual se realizó el fork en la Pregunta 1), en la descripción colocar el link de su repositorio de GitHub.

### En este README, se debe incluir:

- Una explicación del proceso realizado paso a paso.
- Una explicación del **versionamiento semántico**, indicando:
  - En qué consiste.
  - Sus tres componentes (MAJOR, MINOR, PATCH).
  - Ejemplos de aplicación en un proyecto real.
- El enlace al pull request creado hacia el repositorio original.
- Una reflexión sobre la importancia del versionamiento semántico y del uso de forks y pull requests en equipos de trabajo.

**📝 Respuesta:**

<!-- Escribe aquí tu respuesta completa a la Pregunta 6 -->
