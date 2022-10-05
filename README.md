<!-- GIT COMMANDS -->

● git checkout main: nos posicionamos en la rama main.

● git branch: vemos todas las ramas creadas (opcional).

● git pull: nos traemos todos los últimos cambios que hayan sido
mergeados y aprobados en main. Sobre este comando, también tenemos
la posibilidad de usar git pull origin nombreRama para traernos los
cambios de la rama especificada.

● git checkout -b nombreRama: estando posicionados en main, creamos
una nueva rama. Es importante crear una nueva rama para cada nueva
feature/fix así nos evitamos conflictos.

● Realizamos los cambios estando posicionados en la rama previamente
creada.

● git status: vemos que archivos fueron modificados y están listos para ser agregados a un nuevo commit.

● git add nombreDeArchivoModificado: añadimos el archivo indicado al
nuevo commit. En este caso, si tenemos más de un archivo modificado y queremos añadir a todos, podemos hacer git add . con el punto al final para poder añadirlos todos juntos y no ir archivo por archivo.

● git push -u origin nombreRamaDeTrabajo: subimos los cambios a la
rama remota del repositorio. Por ejemplo, si mi rama creada en el paso 4 de esta lista se llamaba feature/login en este paso el comando debería ser git push -u origin feature/login.

● Una vez realizados los pasos anteriores, se abre la posibilidad de hacer un pull request. Para ésto, debemos ir al repositorio en GitHub y hacer click en el botón de color verde que dice “CREATE PULL REQUEST”.

● Uno (o varios) de los colaboradores del repositorio debe aceptar los cambios.

● Una vez que los cambios son aceptados, hacer click en el botón
“CONFIRM SQUASH AND MERGE”. Ésto genera que nuestros cambios
ahora se vean reflejados en la rama main.

● git branch -d nombreRama Si queremos, ahora podemos borrar la rama local creada para ésta tarea en particular.

● git push origin --delete nombreRama Si queremos, ahora podemos borrar la rama global creada para ésta tarea en particular. Esto para el caso de que hayamos creado la rama de manera global q no es lo usual.

● Para realizar una nueva tarea, el ciclo se repite.

Aclaración: tener en cuenta que el orden de los comandos puede verse
afectado dependiendo de lo que se quiera realizar.

<!-- GIT COMMANDS: COMMIT AMEND -->

git log : vemos todos los commits realizados. Para salir de este comando, presionar la tecla q.

git log --oneline : vemos todos los commits realizados en una sola línea. Para salir de este comando, presionar la tecla q.

git commit --amend --no-edit : permite modificar el último commit realizado mientras que no hayas hecho un push. Es importante tener en cuenta que si ya se subió el commit a la rama remota, no se puede modificar. En ese caso, se debe crear un nuevo commit. Hiciste commit y te olvidaste algo e hiciste otro commit.

git commit --amend -m "Mensaje del commit" : permite modificar el último commit realizado.

git reset --hard HEAD~1 : permite deshacer el último commit realizado.

<!-- GIT COMMANDS: MERGE -->

git merge nombreRama: nos posicionamos en la rama en la que queremos mergear los cambios y ejecutamos el comando. Esto nos permite traernos los cambios de la rama especificada a la rama en la que estamos posicionados. Primero tenemos que estar posicionados en la rama en la que queremos mergear los cambios y luego ejecutar el comando.
