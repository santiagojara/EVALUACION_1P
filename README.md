# Universidad [UNIVERSIDAD TECNICA DE AMBATO]  
## Facultad de [Facultad de Ingeniería en Sistemas, Electrónica e Industrial]  
### Carrera de Ingeniería en Software  

**Asignatura:** Manejo y Configuración de Software  
**Nombre del Estudiante:** Erick Aguilar  
**Fecha:** 30/4/2025 

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

**Explicar la diferencia entre los siguientes conceptos/comandos en Git y GitHub:**
- `git clone`  
- `fork`  
- `git pull`
Git clone se usa para "copiar" los archivos que tenemos en un repositorio remoto en git hub
a nuestro repositorio local, a donde nosotros hayamos configurado como repositorio main
Fork es "copiar" los archivos seleccionados de un repositorio y crear un repositorio remoto nuevo 
en la cuenta del usuario que hizo el fork
git pull es un comando que se usa para traer los cambios de una rama remota a una rama local

 ¿Cómo se realizó el fork?
 El fork se realiza unicamente seleccionando el botón de fork que aparece en el repositorio que deseo clonar
 y llenando datos como el nombre que deseo darle al fork y su descripcion
  ¿Cómo se realizó el clone del fork?
  Con el comando git clone seguido del link de mi repositorio fork 
  ¿Cómo se verificó que se estaba trabajando sobre el fork y no sobre el repositorio original?
  Después de clonar el repositorio, ejecuté el comando:git remote -v y mostro mi cuenta como el origin

  [Evidencia de fork realizado](imagenes/cap1.png)

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
Explicación sobre .gitignore

El archivo `.gitignore` se utiliza para indicarle a Git qué archivos o carpetas no deben ser seguidos o versionados. En este caso, se ha configurado el archivo para ignorar todos los archivos con la extensión `.log` y la carpeta `temp/`.
  [Evidencia de fork realizado](imagenes/cap2.png)

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
**📝 Respuesta:**

### Comandos utilizados:

```bash
git flow init
git flow feature start ingresar-encabezado
# (edición del README)
git add README.md
git commit -m "Completar encabezado con mis datos"
git flow feature finish ingresar-encabezado
git push origin develop

Proceso:
Inicialicé Git Flow con git flow init, aceptando las ramas por defecto (main y develop).

Inicié una rama de tipo feature con git flow feature start ingresar-encabezado.

En esta rama edité el encabezado del archivo README.md, agregando mi nombre, materia y fecha.

Realicé un commit con los cambios.

Finalicé la rama feature con git flow feature finish ingresar-encabezado, lo que hizo merge automático hacia develop.

Volvi a la rama main para subir el commit con los cambios que está leyendo ahora mismo

Las ventajas de usar git flow son las de la organización clara y organizada a la hora de desarrollar
distintas partes independientemente.
  [Evidencia de fork realizado](imagenes/cap 3.png)


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

**¿Qué es un issue en GitHub?**  
  Un *issue* es una herramienta de GitHub que permite reportar errores, sugerencias, tareas pendientes o nuevas funcionalidades. Sirve como una forma de gestionar el trabajo colaborativo y de hacer seguimiento de los avances.

- **¿Qué es un pull request?**  
  Un *pull request (PR)* es una solicitud para fusionar cambios desde una rama hacia otra (por ejemplo, de `develop` a `main`). Permite que otros revisen y aprueben los cambios antes de integrarlos, asegurando calidad y coordinación.

- **Diferencia y relación entre ambos:**  
  Un *issue* representa una tarea a realizar o un problema, mientras que un *pull request* es la acción de enviar cambios que posiblemente resuelven ese issue. Están relacionados porque muchas veces un PR cierra o resuelve un issue específico.


**Resumen del procedimiento:**
1. Me aseguré de estar en la rama `develop`.
2. Creé un issue titulado "Respuesta a la Pregunta 4", indicando que su objetivo era documentar esta pregunta.
3. Escribí la teoría y el resumen en esta sección del `README.md`.
4. Hice un commit y lo subí a la rama `develop`.
5. Creé un pull request de `develop` hacia `develop`, vinculando el issue con la línea `Closes #X`.
6. Verifiqué que el repositorio exige una revisión antes de hacer merge, ya que GitHub muestra un mensaje que indica que la fusión está bloqueada hasta recibir aprobación.

**Número del issue creado:** #29
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
