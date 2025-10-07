# Universidad [UNIVERSIDAD TECNICA DE AMBATO]  
## Facultad de [FACULTAD DE INGENIERIA EN SISTEMAS, ELECTRONICA E INDUSTRIAL]  
### Carrera de Ingeniería en Software  

**Asignatura:** Manejo y Configuración de Software  
**Nombre del Estudiante: Sebastian Freire** ___________________________  
**Fecha:10/07/2025** ___________________  

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

<!-- Escribe aquí tu respuesta a la Pregunta 1
- `git clone`
<!--- Este comando nos permite copiar un repositorio completo desde un servidor remoto (como GitHub) hacia nuestra máquina local. Incluyendo todos los archivos, historial de versiones y estructura del proyecto. -->  

<!---- `fork` 
 Permite crear una copia del repositorio original en tu propia cuenta, conservando el vínculo con el original. Es útil para colaborar en proyectos sin modificar directamente el repositorio fuente -->  

<!---- `git pull`
 Este comando se utiliza para actualizar el repositorio local con los últimos cambios del repositorio remoto. Combina git fetch y git merge. -->

<!-- PARTE PRACTICA 
¿Cómo se realizó el fork?
Ingresé al repositorio original en GitHub, hice clic en el botón "Fork" ubicado en la parte superior derecha, y seleccioné mi cuenta personal. GitHub creó automáticamente una copia del repositorio en mi perfil, desde donde estoy trabajando sobre una versión independiente.

¿Cómo se realizó el clone del fork?
Desde mi perfil de GitHub, accedí al repositorio forkeado. Hice clic en el botón verde "Code", seleccioné la opción HTTPS, copié la URL y ejecuté el siguiente comando en la terminal:
git clone https://github.com/TTORNETI/EVALUACION_1P.git

¿Cómo se verificó que se estaba trabajando sobre el fork y no sobre el repositorio original?
Ejecuté el comando git remote -v en la terminal. Esto mostró que el repositorio remoto apuntaba a mi cuenta personal (TTORNETL) y no al repositorio original, confirmando que estaba trabajando sobre el fork.
-->
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

<!-- Escribe aquí tu explicación y evidencia para la Pregunta 2 
<!--
El archivo `.gitignore` se utiliza para indicarle a Git qué archivos o carpetas deben ser ignorados, es decir, no rastreados ni incluidos en el control de versiones.

En este caso, se configuró con las siguientes reglas:

- `*.log`: Ignora todos los archivos con extensión `.log` en cualquier parte del repositorio.
- `temp/`: Ignora completamente la carpeta `temp` y su contenido.
- `doc/*.md` y `doc/*.txt`: Ignora archivos `.md` y `.txt` que estén dentro de la carpeta `doc`.

Para verificar su funcionamiento, se crearon los siguientes archivos de prueba:

1. `error.log` → no aparece en `git status`.
2. `temp/archivo.txt` → no aparece en `git status`.
3. `doc/prueba.md` y `doc/prueba.txt` → no aparecen en `git status`.
4. `prueba.md` y `prueba.txt` (ubicados en la raíz del proyecto) → sí aparecen en `git status`, lo que confirma que `.gitignore` está funcionando correctamente.

Este comportamiento demuestra que Git está respetando las reglas definidas en el archivo `.gitignore`, ignorando únicamente lo que se especificó y permitiendo el rastreo de los archivos que deben mantenerse bajo control de versiones.
-->-->

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
git checkout develop


<!-- # Evaluación - Pregunta 3

**Nombre:** Sebastian Freire   
**Carrera:** Ingeniería en Sistemas  
**Materia:** MANEJO Y CONFIGURACION DEL SOFTWARE - A
**Docente:** [Ing.Santiago Jara]  
**Periodo:** 2025 - 2026 
-->

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
