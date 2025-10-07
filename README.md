# Universidad [Nombre de la Universidad]  
## Facultad de [Nombre de la Facultad]  
### Carrera de Ingeniería en Software  

**Asignatura:** Manejo y Configuración de Software  
**Nombre del Estudiante:** Karen Molina
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

<!-- - `git clone`:Comando de Git que crea una copia local de un repositorio remoto existente, incluyendo todo el historial de commits, ramas y archivos.  

- `fork`: Función de GitHub que crea una copia personal de un repositorio en tu propia cuenta de GitHub, permitiendo trabajar independientemente del repositorio original.

- `git pull`:Comando de Git que descarga los cambios más recientes desde un repositorio remoto y los fusiona automáticamente con la rama actual local.

### Parte práctica:

- Realizar un **fork** de este repositorio en la cuenta personal de GitHub del estudiante.
- Luego, realizar un **clone** del fork en el equipo local.
- En este README, describir el proceso seguido:

  - ¿Cómo se realizó el fork?
      1.Accedí al repositorio original en GitHub desde el link proporcionado por el ingeniero
      2.Hice clic en el botón "Fork" en la esquina superior derecha
      3.Seleccioné mi cuenta personal como destino del fork
      4.GitHub creó una copia completa del repositorio en mi cuenta
      

  - ¿Cómo se realizó el clone del fork?
      Con el comando visto en clase git clone y el link de mi repositorio fork:
      git clone https://github.com/VK0691/EVALUACION_1PMOLINA.git
      ![Img fork](imgs/Screenshot 2025-10-07 151130.png)
      ![Img clone](imgs/Screenshot 2025-10-07 151735.png)
    
  - ¿Cómo se verificó que se estaba trabajando sobre el fork y no sobre el repositorio original?
    Con el comando git remote -v confirmé que la URL apuntaba a mi repositorio personal 
      $ git remote -v
      origin  https://github.com/VK0691/EVALUACION_1PMOLINA.git (fetch)
      origin  https://github.com/VK0691/EVALUACION_1PMOLINA.git (push)
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

<!-- 
*Primer Commit Evidencia:-->
      ![Img ignore](imgs/gitignore.png)

<!--
El archivo .gitignore especifica archivos y directorios que Git debe ignorar y no rastrear. En este caso, se ignoran todos los archivos con extensión .log.
Una carpeta llamada temp/.
Y todos los archivos .md y .txt de la carpeta doc/. 
En la captura adjunta se ve como solo se reflejan los archivos de prueba que no fueron ignorados, mientras que /temp /doc y sus archivos no se ven reflejados -->
      ![Evidencia ignore](imgs/eviignore.png)

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

<!-- Descripción del proceso:
*Comandos exactos usados: 
$ git flow init
$ git flow hotfix start ingresar-encabezado
$ git add .
$ git commit -m "Completar encabezado con datos personales"

*Descripcion del proceso seguido:
Inicialización de Git Flow: Configura el repositorio con la estructura de ramas por defecto (main y develop)

Inicio del feature: Crea una rama feature/ingresar-encabezado a partir de develop

Desarrollo: Realizar los cambios necesarios en la rama feature

Finalización: Fusiona la rama feature en develop y la elimina automáticamente

Reflexión sobre ventajas de Git Flow:
Git Flow proporciona una estructura organizada para el desarrollo de software, especialmente beneficiosa en:

Proyectos colaborativos: Permite que múltiples desarrolladores trabajen en features independientes sin interferir

Larga duración: Facilita el mantenimiento de versiones estables mientras se desarrollan nuevas funcionalidades

Control de calidad: Separa claramente el desarrollo activo (develop) de las versiones estables (main)

Gestion de releases: Estructura definida para preparar releases y hotfixes -->

      ![Img hotfix](imgs/flowhotfix.png)

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
