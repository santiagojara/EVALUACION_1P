# Universidad [Universidad Técnica de Ambato]  
## Facultad de [Ingenierías Industrial, Software y Electrónica]  
### Carrera de Ingeniería en Software  

**Asignatura:** Manejo y Configuración del Software  
**Nombre del Estudiante:** José Gabriel Manzano Bahamonde 
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

Git clone copia todo el repositorio remoto al local, fork es una accion de GitHub que permite proponer cambios a un proyecto de que no se es colaborador, git pull actualiza el repositorio local con los últimos cambios del repositorio remoto.

Para realizar el fork nos fuimos al repositorio remoto y usamos la función para realizarlo. ![alt text](image.png)
El clone del fork nos fuimos a una carpeta que creamos y abrimos bash, ahí escribimos lo siguiente: "git clone https://github.com/JoseM151/EVALUACION_1P_2525.git". 
![alt text](image-1.png)

Para verificar que estamos trabajando en el fork en el mismo GitHub nos dice que el repositorio en el que estamos trabajando esta forkeado desde el repositorio original.

![alt text](image-2.png)

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

### Primer Commit
 ![alt text](image-3.png)

### Segundo Commit
 El archivo .gitignore especifica qué archivos o carpetas deben ser ignoradas por el Git.

Como se puede ver se creo un archivo llamado prueba.log

![alt text](image-4.png)

Y al momento de poner git status no hay rastro del archivo ni de la carpeta creados

![alt text](image-5.png)

Se puso el tag al commit numero 2

![alt text](image-6.png)


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

### Comandos Exactos Usados

git flow init

git flow feature start ingresar-encabezado

git add README.md

git commit -m "Se agregó el nombre completo al encabezado y la fecha"

git commit -m "Se agregó la universidad y la facultad en el encabezado"

git flow feature finish ingresar-encabezado

git tag -a Pregunta3 -m "Commit final de la funcionalidad ingresar-encabezado"

### Descripción del Proceso Seguido

Se inicializó Git Flow con las ramas por defecto main y develop, lo cual permite un desarrollo estructurado y limpio.
Luego se creó una rama de tipo feature/ingresar-encabezado, donde se editó el archivo README.md para incluir los datos personales del estudiante.
Durante el desarrollo, se realizaron varios commits reflejando cambios progresivos. Finalmente, se cerró la feature con git flow feature finish, lo cual integró los cambios a la rama develop.

### Reflexión sobre Git Flow

Git Flow proporciona una estructura clara y organizada para el trabajo colaborativo y el desarrollo de funcionalidades.
Al separar el desarrollo (develop) del código estable (main) y manejar features, releases y hotfixes como ramas especializadas, se evita la contaminación del código en producción.
Este enfoque mejora la trazabilidad de los cambios, facilita el control de versiones y permite mantener flujos de trabajo limpios incluso en equipos grandes o proyectos a largo plazo.

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

### Qué es un Issue?
Un issue es una herramienta de seguimiento que permite registrar tareas, mejoras, errores o solicitudes relacionadas con un proyecto. En un equipo, se usa para coordinar qué debe hacerse, discutir problemas y asignar responsabilidades. Cada issue puede tener comentarios, etiquetas, responsables y una relación directa con commits o pull requests.

### Qué es un Pull Request?
Un pull request (PR) es una solicitud para fusionar los cambios realizados en una rama con otra, generalmente desde una rama feature o develop hacia main o develop. Permite que otros revisen el código antes de que se integre al repositorio, facilitando control de calidad, colaboración y revisión de código entre equipos.

### Diferencias
 La principal diferencia radica en que el issue se usa para planificar y discutir qué se debe hacer, mientras que el pull request muestra cómo se hizo y permite revisar el código antes de integrarlo. Ambos se relacionan directamente en entornos colaborativos: un issue puede originar un pull request, y este último puede cerrarlo automáticamente al completarse, asegurando trazabilidad y organización en el flujo de trabajo.

### Resumen

Se trabajó en la rama develop del repositorio configurado con Git Flow. Primero, se creó un issue titulado "Respuesta a la Pregunta 4" para documentar esta parte del trabajo. Luego, se editaron los contenidos del archivo README.md para incluir la parte teórica y práctica solicitadas. Los cambios fueron confirmados mediante un commit y se subieron a la rama develop en el repositorio remoto. Posteriormente, se generó un pull request desde develop hacia develop en GitHub, el cual fue vinculado al issue creado mediante la instrucción Closes #X. Finalmente, se verificó que el repositorio requiere una revisión previa antes de aceptar el merge, según la configuración de protección de ramas mostrada por GitHub.

### Número del Issue Creado: #6

### Enlace al Pull request

https://github.com/santiagojara/EVALUACION_1P_2525/pull/12#issue-3032862567

### Explicación de como se comprobó

GitHub nos dice que necesita que se revise

![alt text](image-7.png)


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

### Procedimiento realizado

1. Se creó la rama `ramaA` desde `main` y se agregó el archivo `archivoA.txt` con el contenido: `Contenido A`.
2. Luego se creó la rama `ramaB` desde `main`, con el mismo archivo `archivoA.txt`, pero con el contenido: `Contenido B`.
3. Al intentar hacer `merge ramaB` sobre `ramaA`, se generó un conflicto en `archivoA.txt`.
4. Se resolvió el conflicto combinando ambos contenidos y se realizó un nuevo commit con el contenido final:
5. Posteriormente, se fusionó la rama `ramaA` hacia `develop`.
6. Se creó un **pull request** desde `ramaA` hacia `develop`, configurado con revisión obligatoria.
7. GitHub mostró el mensaje:  
`"Review required – At least one approving review is required before merging."`
8. Una vez aprobado y fusionado el PR, se eliminaron ambas ramas (`ramaA` y `ramaB`) tanto local como remotamente.


### Enlace al Pull Request

https://github.com/JoseM151/EVALUACION_1P_2525/pull/1#issue-3032877241

### ¿Qué es un conflicto en Git y por qué ocurrió?

Un **conflicto en Git** ocurre cuando dos ramas modifican el mismo archivo en la misma línea o sección y Git no puede decidir automáticamente qué versión conservar.  
En este caso, `ramaA` y `ramaB` modificaron el mismo archivo (`archivoA.txt`) con contenidos diferentes. Al intentar fusionarlas, Git detectó que no podía unir los cambios sin intervención manual, generando el conflicto que fue resuelto combinando ambos contenidos.

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
