# git practica 2
Taller GIT. Práctica 2.
Guarda los comandos realizados, así como los resultados(capturas), integrarlo dentro del mismo repositorio

## Trabajar con un proyecto HTML y un repositorio local.
- Crea una carpeta practica-taller-git en tu pc.
- Inicializa el repositorio. 
 ```bash
 git init
 ```
- Crea el fichero index.html con un html simple.
- Comprueba que el repositorio a detectado el cambio. 
```bash
git status
```
- Añade el fichero al stage. 
```bash
git add index.html.
```
- Confirma los cambios. 
```bash
git commit -m “added index file”
```
- Añade un fichero description.html y edita index.html.
- Comprueba que ha detectado el nuevo fichero y la modificación de index.
```bash
git status
git diff
```
- Crea un fichero TODO.txt de tareas pendientes.
- Comprueba que git ha detectado el nuevo fichero. 
```bash
git status
```
- Ignora el fichero TODO.txt ya que es donde anotaremos nuestras tareas personales y no debe formar parte del proyecto. Para ello crea un fichero .gitignore con la linea TODO.txt.
- Comprueba que ya no detecta el nuevo fichero TODO.txt (si que detectara el .gitignore claro). 
```bash
git status
```
- Añade y confirma el .gitignore.
- Puedes continuar añadiendo ficheros html, css e imágenes para probar el repositorio.


## Haz un fork del repositorio creado para la práctica del taller:
- Entra en https://github.com/
- Accede a tu cuenta.
- Accede al repositorio del profesor https://github.com/lalobarri/git-practica-2.git
- Pulsa el botón fork (parte superior derecha) para crearte una copia del mismo en tu cuenta.
- Clona el repositorio en tu equipo *en otra carpeta diferente que la llamaremos 'git-practica-2'*. Quedará algo parecido a lo siguiente:
```bash
git clone https://github.com/[tu-nombre-de-usuario]/git-practica-2.git
```
- Crea un nuevo fichero en el proyecto que se llame [tu-nombre-de-usuario].html
- Edita el fichero añadiendo como título tu nombre, algún texto y lo que desees en el.
- Añade el fichero al repositorio.
- Súbelo al repositorio remoto (github). 
```bash
git push
```
- Crea una rama develop y cámbiate a ella.
```bash
git checkout -b develop
```
- Realiza cambios en el proyecto, confírmalos y súbelos al repositorio remoto.
```bash
git status
git add *
git commit -m "Mensaje del commit..."
git push origin
```
- Desde github crea un pull request de la rama develop a main.
- Fusiona la rama develop con en main. No deberías de tener ningún conflicto.
- Haz nuevos cambios en el proyecto siguiendo el flujo de trabajo git flow.


## Preguntas
Crea un nuevo fichero respuestas.md, contesta las siguientes preguntas y súbelo a tu repositorio remoto de github:

 1. ¿Qué sucede cuando hacemos un git add?
 2. ¿Qué sucede cuando hacemos un git commit? ¿Dónde está ese commit? 
 3. ¿Por qué al hacer git commit todavía no está disponible ese commit en el repositorio remoto?
 4. ¿Qué hay que hacer para que veamos este commit en nuestro repositorio remoto de github?
 5. ¿Qué diferencia hay entre hacer un fork o crear una nueva rama?
 6. ¿Qué comando se utiliza para crear una nueva rama sin cambiarte a ella?
 7. ¿Cuál es la diferencia entre los comandos git switch y git checkout al trabajar con ramas?
 8. ¿Qué es una rama por defecto (como main o master) y por qué es importante?
 9. ¿Qué comando te permite ver la lista de todas las ramas locales de tu repositorio?
 10. En el contexto de Git, explica con tus propias palabras qué es una rama (branch) y cuál es su beneficio principal al trabajar en un proyecto de software
 11. ¿Qué ha pasado con el contenido de la carpeta practica-taller-git? ¿Por qué no la podemos ver en nuestro repositorio remoto de github?


*Utilice un formato que permita distinguir entre sus preguntas y respuestas*

## Respuestas en archivo respuestas.md

## Capturas y Evidencias

![git init](https://github.com/user-attachments/assets/1b48a6d1-f84f-4bcf-9e85-9ab36799fa55)

![git init](https://github.com/user-attachments/assets/ea8c3df9-acea-413d-a252-66302266bcf8)

![git init](https://github.com/user-attachments/assets/9b414ed9-5df5-408a-87bc-032ac364cb0f)

![git init](https://github.com/user-attachments/assets/195246e8-edb4-4191-b677-50b298cf59a0)

![git init](https://github.com/user-attachments/assets/57127f26-6786-453c-970f-acf95a096d14)

![git init](https://github.com/user-attachments/assets/4964ca88-b6ac-4ef6-b42f-5f0d2d2f1167)





