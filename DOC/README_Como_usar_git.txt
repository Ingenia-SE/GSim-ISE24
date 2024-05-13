Este repositorio contiene el código para un proyecto de navegación autónoma que utiliza robots Create 3 y drones en entornos aleatorios, implementado con ROS2.
Ramas del Repositorio
•	main/master: La rama principal del repositorio. Contiene la versión estable y funcional del proyecto.
•	develop: Rama de desarrollo principal. Se utiliza para integrar y probar nuevas características antes de fusionarlas en la rama principal.
•	feature/robot: Rama para el desarrollo de características específicas del robot Create 3.
•	feature/drone: Rama para el desarrollo de características específicas del dron.
•	hotfix: Rama para corregir problemas críticos en la versión actual del proyecto.

Metodología de Funcionamiento con Git
Primero abrir una terminal en VSCode, arriba en los 3 puntos  Terminal  Create new terminal.

1. Clonar el Repositorio
Para clonar el repositorio en tu máquina local, utiliza el siguiente comando:
git clone <url_del_repositorio>
también se puede hacer directamente desde github.com
Comprueba en VSCode que estás en la carpeta donde te has clonado el repositorio

2. Crear una Nueva Rama
Antes de crear una rama comprobar que tienes el repositorio en tu ordenador actualizado
git pull origin master
Antes de empezar a trabajar en una nueva característica, crea una nueva rama a partir de la rama develop 
Para ver en que rama estás lo puedes ver abajo izquierda en VSCode o con el comando:
git branch
La rama en la que estás sale con *
git checkout -b feature/<nombre_de_la_caracteristica> develop
Si la rama ya estaba creada:
git checkout feature/<nombre_de_la_caracteristica>

3. Hacer Cambios y Cometerlos
Realiza tus cambios en los archivos necesarios y luego añade los cambios al área de preparación (staging area) utilizando el siguiente comando:
git add <archivos_modificados>
Si quieres añadir todos los cambios a la vez:
git add --all
Una vez que hayas añadido los cambios al área de preparación, realiza un commit con un mensaje descriptivo utilizando el siguiente comando:
git commit -m "Mensaje descriptivo de los cambios realizados"

4. Fusionar la Rama de Característica
Cuando hayas completado y probado que todo funciona, es hora de fusionarla con la rama develop. Primero, asegúrate de estar en la rama develop:
git checkout develop 
Luego, fusiona la rama de la característica con develop:
git merge --no-ff feature/<nombre_de_la_caracteristica>

5. Subir los Cambios al Repositorio Remoto
Una vez que hayas completado y probado tus cambios localmente, es hora de subirlos al repositorio remoto. Primero, asegúrate de estar en la rama correcta:
git checkout <nombre_de_la_rama> 
Luego, sube tus cambios utilizando el siguiente comando:
git push origin <nombre_de_la_rama>

6. Solicitar una Fusión (Pull Request)
Finalmente, solicitar una fusión (pull request) para que tus cambios sean revisados por otros colaboradores antes de fusionarlos con la rama principal. Esto se puede hacer a través de la interfaz web de GitHub.
Al hacer el comando anterior te aparece un link que copias y pegas en Chrome.
Poner en destino el nombre de la rama y pinchar en crear pull request, poner como supervisor a AdelCampoGit (Alex)

Para actualizar los cambios en local una vez aprobados por Alex
git checkout nombrerama
git pull origin nombrerama
