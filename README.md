# Universidad [Nombre de la Universidad]  
## Facultad de [Nombre de la Facultad]  
### Carrera de Ingeniería en Software  

**Asignatura:** Manejo y Configuración de Software  
**Nombre del Estudiante:** Santiago Sebastian Mora Beltran 
**Fecha:** 10/07/2025

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

 -Las diferencias son que git clone sirve para clonar o copiar un repositorio remoto a mi repositorio local, mientras que fork es realizar una copia de un repositorio remoto en mi cuenta de GitHub, por ultimo git pull es un comando para traer la informacion de un repositorio remoto a mi repositorio local.
 -**¿Cómo se realizó el fork?** El fork se realizo en GitHub ubicandonos en el repositorio remoto del docente =, aplastando fork dandole un nombre y solo trayendo la rama main.
 ![Fork realizado](img/image.png)
 -**¿Cómo se realizó el clone del fork?** se cogio el url del clone y se utilizo en git el comando git clone "URL".
 ![clone realizado](img/Screenshot%202025-10-07%20152441.png)

 -**¿Cómo se verificó que se estaba trabajando sobre el fork y no sobre el repositorio original?** se verifico con ayuda del comando git remote -v.

 ![verificacion](img/Screenshot%202025-10-07%20152531.png)

 -commit realizado

 ![commit realizado](img/Screenshot%202025-10-07%20152801.png)
 ![tag y push](img/Screenshot%202025-10-07%20153114.png)

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

-Creacion del archivo .gitignore

![.gitignore](img/Screenshot%202025-10-07%20153257.png)

-configuracion del archivo .gitignore

![configuracion](img/Screenshot%202025-10-07%20153559.png)

-realizacion del primer commit

![1 commit](img/Screenshot%202025-10-07%20153731.png)

-creacion de los archivo y carpeta

![creacion](img/Screenshot%202025-10-07%20153940.png)

-evidencias antes del segundo commit

![evidencia](img/Screenshot%202025-10-07%20154142.png)

-segundo commit 

![2 commit](img/Screenshot%202025-10-07%20154331.png)

![commits](img/Screenshot%202025-10-07%20154852.png)

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

-Inicializacion de git flow

![git flow](img/Screenshot%202025-10-07%20155152.png)

-creacion de la rama hotfix/ingresar-encabezado

![rama](img/Screenshot%202025-10-07%20155324.png)

-commit despues de llenar el encabezado

![commit](img/Screenshot%202025-10-07%20155546.png)

-finalizacion de la rama hotfix

![finalizacion](img/Screenshot%202025-10-07%20155948.png)

-los comando que se utilizaron fueron:
-git flow init
-git flow hotfix start ingresar-encabezado
-git add .
-git commit -m 
-git flow hotfix finish ingresar-encabezado

-Primero se inicializo git flow para posteriormente crear todas las ramas, se crea la nueva rama de hotfix, se anade y se realiza el commit, por ultimo se finaliza la rama hotfix donde se realiza automaticamente el merge.

-Es util aplicar git flow ya que permite ver los cambios y ademas permite al equipo de trabajo trabajar en paralelo sin conflictos gracias a la creacion de diferentes ramas.

-commits
![comits](img/Screenshot%202025-10-07%20160642.png)



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

-Un issue es una herramienta que nos permite seguir el proyecto y reportar errores
-Un pull request es una solicitud para fucionar cambios
-El issue identifica problemas mientras que el pull request fusiona cambios, en un entorno de trabajo los issues permiten organizar los el trabajo mientras que el pull request permite revisar los cambios.

-creacion de la issue

![issue](img/Screenshot%202025-10-07%20161754.png)

-commit y push a devvelop remoto

![develop](img/Screenshot%202025-10-07%20161958.png)

-creacion y vinculacion del pull request

![creacion](img/Screenshot%202025-10-07%20162147.png)

-aceptacion del merge

![merge](img/Screenshot%202025-10-07%20162229.png)

-se creo primero un issue en github para despues realizar los cambios que se requerian por ultimo se solicito un pull request hacian main de develop para responder al issue y ademas se acepto el merge
-**Issue** #1 https://github.com/Santio13-code/EVALUACION_1P/issues/1#issue-3493074715
-**Pull Request** #2 https://github.com/Santio13-code/EVALUACION_1P/pull/2#issue-3493083920

-comits

![comits](img/Screenshot%202025-10-07%20163018.png)

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

-creacion de las ramas

![ramas](img/Screenshot%202025-10-07%20163239.png)

-archivo ramaA

![archivo](img/Screenshot%202025-10-07%20163430.png)

-archivo ramaB

![archivo](img/Screenshot%202025-10-07%20163608.png)

- generacion del conflicto

![conflicto](img/Screenshot%202025-10-07%20163726.png)

-resolucion del conflicto
![resolucion](img/Screenshot%202025-10-07%20163848.png)

-merge hacia develop de ramaA

![merge](img/Screenshot%202025-10-07%20163947.png)




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
