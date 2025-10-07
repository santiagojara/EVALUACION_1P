# Universidad Tecnica de Ambato  
## Facultad de Ingeniería en Sistemas, Electrónica e Industrial  
### Carrera de Ingeniería en Software  

**Asignatura:** Manejo y Configuración de Software  
**Nombre del Estudiante:** Pillapa Tubon Wilson joseh 
**Fecha:** 7-10-2025  

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

git clone: Es un comando de Git que crea una copia completa de un repositorio remoto en tu máquina local. Descarga todo el historial de commits, ramas y archivos del repositorio. Se usa con git clone 

fork: Es una funcionalidad de GitHub que crea una copia completa de un repositorio en tu cuenta personal de GitHub. Es independiente del repositorio original y te permite hacer cambios sin afectar el proyecto original. Es útil para contribuir a proyectos de código abierto.

git pull: Es un comando de Git que descarga los cambios del repositorio remoto y los fusiona automáticamente con tu rama local actual. Es una combinación de git fetch + git merge.

- ¿Cómo se realizó el fork?
Entra al repositorio original en GitHub https://github.com/santiagojara/EVALUACION_1P y hacemos click en la parte quqee dice fork

- ¿Cómo se realizó el clone del fork?
Copié la URL HTTPS de mi fork https://github.com/W1LSONN/EVALUACION_1P.git.
y luego en el git bash ingrese el comando git clone https://github.com/W1LSONN/EVALUACION_1P.git
Esto creó una copia local del fork bajo la carpeta 

- ¿Cómo se verificó que se estaba trabajando sobre el fork y no sobre el repositorio original?
ejecutamos el siguiente comando:
$ git remote -v
origin  https://github.com/W1LSONN/EVALUACION_1P.git (fetch)
origin  https://github.com/W1LSONN/EVALUACION_1P.git (push)
y ahi nos muestra que estamos trabaja en el repositorio de nosotros y no en el del ingeniero.


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

El archivo `.gitignore` es un archivo de configuración de Git que especifica qué archivos o carpetas deben ser ignorados por el sistema de control de versiones. Esto significa que Git no rastreará, ni incluirá en commits, ni subirá al repositorio remoto los archivos o carpetas que coincidan con los patrones definidos en `.gitignore`.

Es útil para:
- Evitar subir archivos temporales o de log
- Excluir carpetas de dependencias (node_modules, venv, etc.)
- Ignorar archivos de configuración local
- Mantener el repositorio limpio y enfocado en el código fuente

**Reglas configuradas:**
1. `*.log` - Ignora todos los archivos con extensión .log en cualquier ubicación
2. `temp/` - Ignora completamente la carpeta temp y todo su contenido
3. `doc/*.md` y `doc/*.txt` - Ignora archivos .md y .txt solo dentro de la carpeta doc/

Al ejecutar `git status` después de crear los archivos de prueba, se observa:

-Los archivos `test.log` NO aparecen (ignorados por `*.log`)
-la carpeta `temp/` NO aparece (ignorada por `temp/`)
-Los archivos `doc/prueba.md` y `doc/prueba.txt` NO aparecen (ignorados por `doc/*.md` y `doc/*.txt`)
-Los archivos `prueba.md` y `prueba.txt` en la raíz SÍ aparecen como untracked files, porque solo se ignoran dentro de la carpeta doc/, no en la raíz del proyecto
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

Paso 1 - Inicialización: La inicialización de Git Flow establece la estructura de ramas necesaria para seguir este flujo de trabajo, definiendo main como rama de producción y develop como rama de desarrollo.
Paso 2 - Creación del hotfix: Al crear un hotfix, se genera una rama temporal desde main para realizar correcciones urgentes o cambios menores que deben aplicarse directamente a producción.
Paso 3 - Modificación y commit: Se completa el encabezado del documento con los datos personales del estudiante y se registra el cambio mediante un commit.
Paso 4 - Finalización: Al finalizar el hotfix, Git Flow automáticamente:

Integra los cambios en main (producción)
Crea un tag para marcar esta versión
Integra los cambios en develop para mantener sincronización
Elimina la rama temporal del hotfix

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

**Parte Teórica:**

**¿Qué es un Issue en GitHub?**

Un issue es una herramienta de GitHub que permite rastrear tareas, errores (bugs), mejoras o cualquier tipo de trabajo pendiente en un proyecto. Funciona como un sistema de tickets donde se pueden:
- Reportar problemas o errores
- Proponer nuevas funcionalidades
- Hacer preguntas sobre el proyecto
- Documentar tareas pendientes
- Asignar responsables
- Etiquetar por categorías
- Comentar y discutir soluciones

**¿Qué es un Pull Request y cuál es su finalidad?**

Un Pull Request (PR) es una solicitud para fusionar cambios de una rama a otra. Su finalidad principal es:
- Proponer cambios al código del proyecto
- Permitir la revisión de código antes de integrarlo
- Facilitar la discusión sobre los cambios propuestos
- Mantener un historial de qué cambios se hicieron y por qué
- Ejecutar pruebas automáticas antes del merge
- Garantizar calidad del código mediante revisión por pares

**Diferencia y relación entre Issues y Pull Requests:**

**Diferencias:**
- Un **Issue** identifica un problema o tarea (el "qué")
- Un **Pull Request** propone una solución mediante código (el "cómo")
- Los Issues no contienen código, los PR sí
- Los Issues pueden existir sin PR, pero los PR suelen resolver Issues

**Relación en trabajo colaborativo:**
En un flujo de trabajo típico:
1. Se crea un **Issue** describiendo un problema o tarea
2. Un desarrollador trabaja en una rama para resolver ese Issue
3. Se crea un **Pull Request** con los cambios, referenciando el Issue
4. El equipo revisa el PR
5. Una vez aprobado, se hace merge y el Issue se cierra automáticamente

Esta relación permite trazabilidad completa: desde la identificación del problema hasta su solución.

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
