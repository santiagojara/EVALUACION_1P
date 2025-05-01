# Universidad Universidad Tecnica de Ambato
## Facultad de Ingeniería en Sistemas Electrónica y Industrial
### Carrera de Ingeniería en Software  

**Asignatura:** Manejo y Configuración de Software  
**Nombre del Estudiante:** TOALA CAMACHO STEEVEN SANTIAGO
**Curso:** 4to Software A
**Fecha:** 30/04/2025 

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

<!-- Escribe aquí tu respuesta a la Pregunta 1 -->
-git clone copia un repositorio remoto a tu computadora, fork crea una copia del repositorio en tu cuenta de GitHub desde la web, y git pull actualiza tu copia local con los últimos cambios del remoto.
-Para realizar el fork, ingresé al repositorio original en GitHub:
https://github.com/santiagojara/EVALUACION_1P_2525.
Luego, hice clic en el botón "Fork" ubicado en la parte superior derecha de la página. Seleccioné mi cuenta personal de GitHub como destino. Esto creó una copia del repositorio en mi propia cuenta.
-Una vez que el fork se creó en mi cuenta personal de GitHub, accedí a la URL del repositorio forkeado
Luego, en la terminal de mi equipo, ejecuté el siguiente comando para clonar el fork:
git clone https://github.com/SteevenToala/EVALUACION_1P_2525.git
-Ingresé a la carpeta del repositorio clonado y ejecuté el siguiente comando:
git remote -v
La salida mostró que el repositorio remoto (origin) apuntaba a mi cuenta personal de GitHub, por ejemplo:
origin  https://github.com/SteevenToala/EVALUACION_1P_2525.git (fetch)
origin  https://github.com/SteevenToala/EVALUACION_1P_2525.git (push)

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

<!-- Escribe aquí tu explicación y evidencia para la Pregunta 2 -->
Se creo el archivo .gitignore y se puso lo que se va a ignorar al ejecutar el comando git add .
temp/
*.log
esta carpeta y archivo no se van a agregar al area de preparacion.
![alt text](image.png)
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

<!-- Escribe aquí tu respuesta completa a la Pregunta 3 -->
-Descripción del proceso seguido:
1.Inicialización de Git Flow: Inicialicé Git Flow para establecer las ramas main y develop, lo que define una estructura ordenada para el flujo de trabajo de desarrollo y producción.
2.Creación de la rama feature/ingresar-encabezado: Creé una nueva rama feature para trabajar en la funcionalidad ingresar-encabezado, asegurando que las nuevas características no afectaran la rama principal develop.
3.Desarrollo y commit: Realicé los cambios en el archivo README.md, agregando los datos personales del estudiante, y luego realicé un commit para guardar el progreso.
4.Finalización de la rama feature: Tras completar la funcionalidad, utilicé git flow feature finish para fusionar la rama feature con develop, lo que asegura que la nueva funcionalidad se integre de manera controlada.

-Reflexión sobre las ventajas de aplicar Git Flow:
Organización y control: Git Flow proporciona una estructura clara para organizar el desarrollo, especialmente en proyectos grandes y colaborativos. Las ramas feature, develop, y main aseguran que las nuevas funcionalidades se desarrollen y prueben de forma aislada antes de llegar a producción.
Facilita la colaboración: Al usar ramas específicas para cada funcionalidad, diferentes miembros del equipo pueden trabajar simultáneamente en diversas tareas sin interferir entre sí. Git Flow también facilita la integración de cambios mediante pull requests.
Flujo controlado de versiones: Git Flow ayuda a gestionar el ciclo de vida de cada versión del software, desde el desarrollo hasta la producción, permitiendo un flujo controlado de nuevas características y correcciones urgentes.


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
PARTE TEORICA
1.¿Qué es un issue en GitHub?

Un issue en GitHub es una herramienta para registrar, discutir y realizar un seguimiento de tareas, errores o solicitudes de mejora dentro de un proyecto. Los issues se pueden usar para reportar bugs, proponer nuevas características o discutir cualquier aspecto del proyecto. Cada issue tiene un título, una descripción y puede incluir comentarios, etiquetas, asignaciones, y una fecha de vencimiento. Los issues permiten gestionar de manera organizada los trabajos pendientes o problemas dentro de un repositorio.

2.¿Qué es un pull request y cuál es su finalidad?

Un pull request (PR) es una solicitud para que los cambios realizados en una rama sean revisados e integrados en otra rama, típicamente en la rama main o develop. Su finalidad es permitir que el código que se ha desarrollado en una rama separada sea evaluado por otros colaboradores antes de fusionarse con la rama principal del proyecto. Los pull requests facilitan la colaboración, la revisión del código y la detección de errores, mejorando la calidad del código y asegurando que las integraciones sean controladas.

3.Diferencia entre un issue y un pull request:

Issue: Es una tarea o un problema que necesita ser abordado. Los issues son utilizados principalmente para seguir el progreso de tareas específicas, ya sean correcciones de errores, nuevas funcionalidades o discusiones generales.

Pull request: Es un mecanismo que se utiliza para integrar cambios en el código entre ramas diferentes. El pull request está vinculado a la revisión de código y su fusión en una rama principal.

En un entorno de trabajo colaborativo, los issues se crean para identificar trabajos o problemas, y luego se vinculan con pull requests que resuelven esos problemas o implementan las tareas solicitadas. El flujo típico es que se crea un issue, se desarrolla una solución en una rama separada, se crea un pull request para revisarlo y, una vez aprobado, el pull request se fusiona y el issue se cierra.

PARTE PRACTICA
Resumen del procedimiento realizado:
Creación del issue: Se creó un issue titulado "Respuesta a la Pregunta 4" en GitHub para documentar la explicación teórica sobre issues y pull requests. Este issue tiene como objetivo proporcionar contexto sobre la pregunta planteada.

Realización de cambios en el archivo README.md: Se realizaron las modificaciones necesarias en el archivo README.md para responder la pregunta 4, proporcionando la explicación teórica y práctica de los conceptos solicitados.

Commit y subida a la rama develop: Los cambios realizados en el archivo README.md fueron comprometidos y subidos a la rama develop con el siguiente comando:

git add README.md
git commit -m "Se agregó la respuesta a la Pregunta 4"
git push origin develop
Creación del pull request: Se creó un pull request desde la rama develop hacia la misma rama develop en GitHub. Esto permitió una revisión y fusión de los cambios documentales realizados.
https://github.com/santiagojara/EVALUACION_1P_2525/pull/8
Vinculación del pull request con el issue: En el cuerpo del pull request, se incluyó una referencia al issue creado, utilizando ClosesS #8 para vincularlo. Esto asegura que cuando el pull request sea fusionado, el issue se cerrará automáticamente.

Revisión antes del merge: Al revisar el pull request en GitHub, se observó que se requería una revisión previa antes de fusionar los cambios. El mensaje en GitHub indicaba que el pull request debía ser aprobado antes de su fusión. Este requisito de revisión es una configuración de protección de ramas en el repositorio.
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

Procedimiento completo:
Creación de las ramas:
git checkout main
git pull origin main
git checkout -b ramaA
git checkout main
git checkout -b ramaB

Modificación de archivoA.txt en cada rama:

En ramaA:
echo "Contenido A" > archivoA.txt
git add archivoA.txt
git commit -m "Agregar archivoA.txt con Contenido A"
git push origin ramaA

En ramaB:
echo "Contenido B" > archivoA.txt
git add archivoA.txt
git commit -m "Agregar archivoA.txt con Contenido B"
git push origin ramaB

Generación del conflicto al intentar fusionar ramaB en ramaA:
git checkout ramaA
git merge ramaB

Resolución del conflicto:

El archivo archivoA.txt fue editado para contener:
Contenido combinado A+B

Luego se continuó con:
git add archivoA.txt
git commit -m "Resolver conflicto combinando contenido A y B"
git push origin ramaA

Fusión de ramaA en develop:
git checkout develop
git pull origin develop
git merge ramaA
git push origin develop

Creación del Pull Request:

Se creó un pull request desde ramaA hacia develop en GitHub.
Enlace al pull request: 

Verificación de revisión requerida:

GitHub mostró el mensaje:
"Review required. At least one approving review is required by reviewers with write access before merging."

Eliminación de ramas tras el merge:

Local:
git branch -d ramaA
git branch -d ramaB

Remoto:
git push origin --delete ramaA
git push origin --delete ramaB



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
