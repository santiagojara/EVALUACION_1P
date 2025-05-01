# Universidad [Universidad Técnica de Ambato]  
## Facultad de [FISEI]  
### Carrera de Ingeniería en Software  

**Asignatura:** Manejo y Configuración de Software  
**Nombre del Estudiante:** ___Bryan Lopez________________________  
**Fecha:** _____30/04/2025______________  

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

- `git clone `: copia un repositorio completo desde un servidor remoto a tu computadora (repositorio local).  
- `fork` :  crea una copia personal completa de un repositorio ajeno en tu propia cuenta dentro de esa misma plataforma.
- `git pull`: actualiza tu repositorio local trayendo los cambios desde un repositorio remoto al que está conectado (normalmente llamado origin, que suele ser tu fork o el repositorio original si no has hecho fork).

### Parte práctica:

- Realizar un **fork** de este repositorio en la cuenta personal de GitHub del estudiante.
- Luego, realizar un **clone** del fork en el equipo local.
- En este README, describir el proceso seguido:
  - ¿Cómo se realizó el fork?
  - ¿Cómo se realizó el clone del fork?
  - ¿Cómo se verificó que se estaba trabajando sobre el fork y no sobre el repositorio original?

**📝 Respuesta:**

<!-- Escribe aquí tu respuesta a la Pregunta 1 -->
-¿Cómo se realizó el fork?
El fork se realiza directamente en la plataforma web donde está alojado el repositorio original.
Navegamos a la página principal del repositorio original que se desea copiar.
Buscamos y hacemos clic en el botón "Fork". 
La plataforma creará automáticamente una copia completa del repositorio bajo tu cuenta. Nos redirige a la página de este nuevo repositorio (mi fork). 

-¿Cómo se realizó el clone del fork?
Nos dirigimos a la pagina de nuestro fork, en git Bash nos dirijimos a nuestra carpeta remota con el comando cd "url de la carpeta en nuestro dispositivo",ejecutamos el comando git clone y la url de nuestro repositorio, en este caso: https://github.com/BryanLopez257/EVALUACION_1P_2525.git

-¿Cómo se verificó que se estaba trabajando sobre el fork y no sobre el repositorio original?
Se ejecuto el comando remote -v y nos muestra dos repositorios remotos configurados.
<img src="EVALUACION_1P_2525/Imagenes/git remote.png">
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
## Función
El archivo `.gitignore` especifica archivos y carpetas que Git debe ignorar intencionalmente. Los archivos listados en `.gitignore` no serán rastreados por Git, lo que significa que no se añadirán al área de preparación ni se incluirán en los commits, a menos que ya estuvieran siendo rastreados antes de añadir la regla. Es útil para excluir archivos generados automáticamente, logs, dependencias, archivos de configuración local, etc.

## Reglas Configuradas
En este repositorio, el archivo `.gitignore` se ha configurado con las siguientes reglas:

```gitignore
# Ignorar todos los archivos con extensión .log
*.log

# Ignorar la carpeta temp y todo su contenido
temp/

---
<img src="EVALUACION_1p_2525/Imagenes/git tag.png">

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
Primeramente inicialice git flow con el comando: git flow init -d, seguido a eso inicie la rama de caracteristica feature con el comando: git flow feature start ingresar-encabezado, despues añadi los cambios de README al staging despues de editarlos con el comando: git add README.md, realice el commit intermedio con el comando: git commit -m "", y finalice la rama feature con: git flow feature finish ingresar-encabezado. 
Añadi los cambios de README a stating con git add README.md y realice el commit -m "". Por ultimo, hice el tag del ultimo commit con git tag Pregunta-3 HEAD.
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
¿Qué es un Issue en GitHub?
Un issue (incidencia, problema, o tarea) en GitHub es una herramienta fundamental para el seguimiento del trabajo dentro de un repositorio.

¿Qué es un Pull Request (PR) y cuál es su finalidad?
Un Pull Request (PR) o Solicitud de Extracción en GitHub es el mecanismo principal para proponer cambios a un repositorio. 

Diferencia entre Issue y Pull Request y su Relación
Issue: Describe qué necesita hacerse, mejorarse o arreglarse. Es el "problema" o la "tarea". Se enfoca en el seguimiento y la discusión del trabajo pendiente.
Pull Request: Propone una solución específica (un conjunto de cambios en el código) para un issue o para añadir una nueva funcionalidad. Es la "propuesta de cambio" lista para revisión e integración.

Relación en Entorno Colaborativo:
Se relacionan estrechamente:
Un issue se crea primero para identificar y describir un trabajo a realizar (ej. "Issue #15: Arreglar error de login").
Un desarrollador toma ese issue, crea una rama (ej. fix/login-bug) y trabaja en la solución.
Una vez que tiene la solución lista en su rama, crea un Pull Request desde su rama (fix/login-bug) hacia la rama principal de desarrollo (develop).
Crucialmente, vincula el Pull Request al Issue (ej. escribiendo "Closes #15" en la descripción del PR).
El equipo revisa el código en el PR.
Una vez aprobado y fusionado el PR, GitHub puede cerrar automáticamente el Issue vinculado (#15), indicando que el trabajo está completado e integrado.
Este flujo conecta el problema (Issue) con su solución propuesta y revisada (Pull Request), manteniendo la trazabilidad del trabajo.
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
