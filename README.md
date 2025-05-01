# Universidad [Nombre de la Universidad]  
## Facultad de [Nombre de la Facultad]  
### Carrera de Ingeniería en Software  

**Asignatura:** Manejo y Configuración de Software  
**Nombre del Estudiante:** Saimol Steph Jimenez Chango  
**Fecha:** 30 de Abril del 2025  

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

**git Clone**: clona un repositorio remoto completo (incluyendo historial y ramas) a tu máquina local, estableciendo una conexión (llamada origin por defecto) con el repositorio remoto del cual se clonó.

**fork:** Es una acción en plataformas como GitHub que crea una copia personal de un repositorio ajeno dentro de la misma plataforma. Permite experimentar o proponer cambios sin afectar el original.

**git pull:**  actualiza tu repositorio local trayendo los cambios desde el repositorio remoto y fusionándolos (Workspace + merge) en tu rama local actual.

  - ¿Cómo se realizó el fork?
1. se inicio seccion en Github
2. Se Navego al repositorio destino
3. Se hizo clic en Fork 

  ![Verdicacion del fork](img/captura1.png)

  - ¿Cómo se realizó el clone del fork?

Se realizo desde el Git Bash, primero se creo la carpeta donde se va a ubicar el fork y luego se uso el siguiente comando ``` git clone https://github.com/saimol-h1/EVALUACION_1P_2525 ```. Luego se ingreso ala carpeta creada.

![Verficacion del fork](img/captura2.png)
  - ¿Cómo se verificó que se estaba trabajando sobre el fork y no sobre el repositorio original?

Para saber que estamos trabajando sobre un fork se realiza el siguiente comando ```git remote -v```

![Verficacion del fork](img/captura3.png)


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

El .gitignore es para especificar archivos/patrones que Git debe ignorar y no rastrear, como archivos de configuración local, logs, dependencias, etc.

Dentro del .gitignore se coloco lo siguiente
```
*.log
temp/
```
Se muestra que se ignora:

![se ve que los archivos son ignorados](img/captura5.png)

Se comprueba lo que se ignora:
![se ve que solo NoseIgnora.txt](img/captura4.png)

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

git flow init 
git flow feature start ingresar-encabezado
git add .
git commit -m "Se agrego los datos del estudinate"
git flow feature finish ingresar-encabezado

Se inicio el flujo de trabajo con ```git flow init``` y luego de la instalacion se creo la rama feature (aislar desarrollo de nueva funcionalidad), luego de realizar los cambios se realizo el commit (guardar progreso), al final se uso el comando ```git flow feature finish``` finalización de la feature (integrar cambios en develop y limpiar).

Es útil por la estructura clara (separación main/develop/feature/release/hotfix), facilita el trabajo paralelo en equipo, la gestión de versiones y lanzamientos, y mantiene la rama main siempre estable.

![se ve que solo NoseIgnora.txt](img/captura6.png)

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

Qué es un Issue:
Un Issue en GitHub es una herramienta de seguimiento utilizada para gestionar tareas, errores (bugs), mejoras, o cualquier otro tipo de trabajo relacionado con el proyecto. Los issues permiten organizar y priorizar lo que se debe hacer, y se pueden usar para discutir soluciones, asignar tareas a los colaboradores y realizar un seguimiento del progreso. Esencialmente, un issue ayuda a mantener el control sobre los aspectos del proyecto que necesitan atención.

Qué es un Pull Request:
Un Pull Request (PR) es una solicitud que realiza un colaborador para fusionar cambios desde una rama hacia otra dentro de un repositorio. Los PRs facilitan la revisión del código y permiten que los miembros del equipo discutan sobre los cambios propuestos antes de aceptarlos. A través de un pull request, otros miembros del equipo pueden revisar, sugerir mejoras y aprobar el código antes de que sea integrado en la rama principal del proyecto, como main o develop.

Diferencia y Relación:
Diferencia: Un Issue define qué se necesita hacer, como corregir un error, agregar una nueva funcionalidad o mejorar una parte del código. Un Pull Request, en cambio, describe cómo se va a implementar esa tarea o solución (el código necesario para completar la tarea del Issue).

Relación: Los Pull Requests a menudo se vinculan a un Issue específico para indicar qué problema o tarea están resolviendo. Esta vinculación permite un seguimiento claro y transparente de qué cambios están destinados a resolver problemas o completar tareas específicas. Por ejemplo, un PR puede cerrarse automáticamente cuando el Issue relacionado se resuelve mediante la fusión del código propuesto.

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
