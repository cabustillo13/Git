# GIT NOTAS

## **CLASE 1**

#### Git vrs Github
* Git: Herramienta para el control de versiones.
* Github: Servicio que aloja tus proyectos.

#### Áreas en git
Directorio de trabajo -> Staging Index -> Repositorio

Viene a representar como es el flujo de trabajo cuando pasas algún archivo que estamos tratando localmente y cargarlo al repositorio.
Cuando se realiza una commit, solo los cambios que se encuentran en el Staging Index se guardan en el repositorio.

*EJEMPLO: El archivo HTML tiene cambios de HTML y CSS en el Staging Index y un cambio adicional de HTML en el directorio de trabajo. ¿Qué crees que se comprometerá si se realiza un compromiso en este momento? R// Solo el HTML y CSS que están en el Staging Index.* 

## **CLASE 2**

#### git clone

*CONSEJO: Ahora, antes de clonar algo, asegúrese de estar ubicado en el directorio correcto en la línea de comando. La clonación de un proyecto crea un nuevo directorio y coloca el repositorio Git clonado en él. El problema es que no puedes tener repositorios Git anidados. Así que asegúrese de que el directorio de trabajo actual de la terminal no esté ubicado en un repositorio Git. Si su directorio de trabajo actual no está en la línea de comandos de su shell, escriba pwd para imprimir el directorio de trabajo.*

#### git status

Es un comando muy útil, que nos permite principalmente:
* Nos dice acerca de los nuevos archivos que se han creado en el Directorio de trabajo que Git aún no ha comenzado a rastrear.
* Archivos que Git está rastreando que han sido modificados.

## **CLASE 3**

#### git log

Devuelve información sobre los commits existentes.

#### git show

Devuelve información sobre un commit dado. Tipo vos le mandas el SHA de un commit específico y te devuelve toda la información solo de ese commit.

*CONSEJO: Siempre debe ejecutar el comando git status. Especialmente al regresar a un proyecto después de un período de tiempo.*

## **CLASE 4**

#### git add

Permite agregar archivos desde el directorio de trabajo al staging index.

#### git commit

Permite tomar los archivos del staging index para guardarlos en el repositorio.

#### git diff

Permite ver la diferencia entre dos versiones de un archivo. Este comando se usa para ver los cambios que se han realizado pero que aún no se han confirmado (osea aún no se realiza el commit).

El output que devuelve es similar a ```git log -p```.

*DATO: Ejecutar ```git init``` varias veces no causa ningún problema, ya que solo reinicia el directorio Git.*

#### Consejos de las personas de Udacity

*CONSEJO: La imagen fue obtenida del curso de [Version Control with Git - Udacity](https://www.udacity.com/course/version-control-with-git--ud123).*

![Consejo sobre cómo escribir los mensajes para el commit](https://github.com/cabustillo13/Git/blob/master/A%20good%20commit%20message.png)

[Udacity Git Commit Message Style Guide:](https://udacity.github.io/git-styleguide/)



