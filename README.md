## Finalidad
Este proyecto es una prueba de concepto de desarrollo en netcore 2.2 usando como herramientas Visual Studio Code y docker.
## Estado actual de la integración entre VSCode y docker
Hasta el momento se ha logrado que VSCode sea capaz de depurar la aplicación dentro del contenedor.
### Pasos a nivel de configuración del proyecto:
* Creación de un Dockerfile que cree la imagen sobre la que queremos desarrollar. Es muy importante incluir vsdbg (https://aka.ms/getvsdbgsh) dentro de la imagen para que VSCode sea capaz de depurar.
* Creación de un docker-compose que establece el ecosistema en el que debe trabajar la aplicación, en este caso el servidor que contiene la aplicación netcore y otro con una base de datos MySql
* Configuración del proyecto en VSCode para que este sea capaz de depurar en el contenedor modificando .vscode/launch.json
### Pasos para iniciar la depuración:
* Levantar los contenedores con docker-compose up
* Lanzar la depuración seleccionando en la vista de depuración y seleccionar la configuración que se ha creado para trabajar en docker, en nuestro caso "Attach to mod2lab1 (Docker)"
