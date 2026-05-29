# Respuestas - Práctica Git

**Alumno:** Pedro Uriel Pérez

---

## Pregunta 1: ¿Qué sucede cuando hacemos un git add?

**Respuesta:** Al ejecutar `git add`, los archivos seleccionados pasan del directorio de trabajo al área de preparación (staging area o índice). Esto le indica a Git qué cambios queremos incluir en el próximo commit. Los archivos aún no están guardados permanentemente en el historial; solo están "listos" para ser confirmados.

---

## Pregunta 2: ¿Qué sucede cuando hacemos un git commit? ¿Dónde está ese commit?

**Respuesta:** Al hacer `git commit`, Git toma todos los cambios del área de preparación y los guarda de forma permanente en el historial del repositorio local, creando un nuevo punto en la línea de tiempo del proyecto con un identificador único (hash). Ese commit queda almacenado únicamente en el repositorio local de nuestra máquina, dentro de la carpeta `.git`.

---

## Pregunta 3: ¿Por qué al hacer git commit todavía no está disponible ese commit en el repositorio remoto?

**Respuesta:** Porque `git commit` solo guarda los cambios en el repositorio local (nuestra máquina). Git trabaja de forma distribuida: el repositorio local y el repositorio remoto (en GitHub) son independientes. El commit existe en nuestro historial local, pero no se ha enviado al servidor remoto todavía.

---

## Pregunta 4: ¿Qué hay que hacer para que veamos este commit en nuestro repositorio remoto de GitHub?

**Respuesta:** Hay que ejecutar el comando `git push` para enviar los commits locales al repositorio remoto. Esto sincroniza los cambios de nuestra rama local con la rama correspondiente en GitHub, haciéndolos visibles para todos.

---

## Pregunta 5: ¿Qué diferencia hay entre hacer un fork o crear una nueva rama?

**Respuesta:**
- **Fork:** Es una copia completa e independiente del repositorio en otra cuenta de GitHub. Se usa para contribuir a proyectos ajenos sin tener permisos de escritura en el original, o para tener una versión completamente propia del proyecto.
- **Rama (branch):** Es una línea de desarrollo paralela dentro del mismo repositorio. Se usa para trabajar en nuevas funcionalidades o correcciones sin afectar la rama principal, y luego fusionar los cambios.

La diferencia principal es que el fork crea un repositorio separado en GitHub, mientras que la rama existe dentro del mismo repositorio.

---

## Pregunta 6: ¿Qué comando se utiliza para crear una nueva rama sin cambiarte a ella?

**Respuesta:**
```bash
git branch nombre-de-la-rama
```
Este comando crea la rama pero mantiene el puntero HEAD en la rama actual. Para crear Y cambiarte a la vez se usaría `git checkout -b nombre-de-la-rama`.

---

## Pregunta 7: ¿Cuál es la diferencia entre los comandos git switch y git checkout al trabajar con ramas?

**Respuesta:**
- `git checkout`: Es un comando más antiguo y versátil que sirve tanto para cambiar de rama como para restaurar archivos. Su uso múltiple puede generar confusión.
- `git switch`: Es un comando más reciente (Git 2.23+) diseñado específicamente para cambiar entre ramas. Es más claro e intuitivo para esa tarea concreta.

Ambos permiten cambiar de rama, pero `git switch` fue creado para hacer esa acción más explícita y segura.

---

## Pregunta 8: ¿Qué es una rama por defecto (como main o master) y por qué es importante?

**Respuesta:** La rama por defecto es la rama principal del repositorio, que se crea automáticamente al inicializar un proyecto. Es importante porque:
- Representa el estado estable y oficial del proyecto.
- Es la rama que ven los colaboradores y usuarios al acceder al repositorio.
- Sirve como base desde la que se crean otras ramas de desarrollo.
- En entornos de producción, suele ser la rama que se despliega.

---

## Pregunta 9: ¿Qué comando te permite ver la lista de todas las ramas locales de tu repositorio?

**Respuesta:**
```bash
git branch
```
Para ver también las ramas remotas:
```bash
git branch -a
```

---

## Pregunta 10: En el contexto de Git, explica con tus propias palabras qué es una rama (branch) y cuál es su beneficio principal al trabajar en un proyecto de software

**Respuesta:** Una rama es como una línea de tiempo paralela dentro del proyecto. Imagina que el proyecto es un árbol: el tronco principal sería `main`, y las ramas permiten desarrollar nuevas funcionalidades o corregir errores en paralelo sin tocar el código estable del tronco.

El beneficio principal es el **aislamiento**: varios desarrolladores pueden trabajar simultáneamente en distintas partes del proyecto sin interferirse entre sí. Cuando el trabajo está listo y probado, se fusiona (merge) de vuelta a la rama principal de forma controlada.

---

## Pregunta 11: ¿Qué ha pasado con el contenido de la carpeta practica-taller-git? ¿Por qué no la podemos ver en nuestro repositorio remoto de GitHub?

**Respuesta:** La carpeta `practica-taller-git` es un repositorio local independiente que creamos en nuestra máquina en la primera parte de la práctica. No podemos verla en GitHub porque nunca la vinculamos a un repositorio remoto ni hicimos `git push` desde ella. Cada repositorio Git es independiente: tener un repositorio en una carpeta no significa que esté automáticamente disponible en la nube; hay que configurar un remote y hacer push explícitamente para subirlo a GitHub.
