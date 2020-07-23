# Git

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
