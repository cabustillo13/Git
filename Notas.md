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

####  Conceptos

- **Git**: Es una control de versión distribuida, eso quiere decir cada integrante puede tener su propia copia del código en su computadora.

- **SHA**: Es el número de confirmación para cada commit. 

Se ve así: _e2adf8ae3e2e4ed40add75cc44cf9d0a869afeb6_

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

#### .gitignore

Se puede meter todos los archivos que no se quieren observar de forma pública, pero que permanezca localmente.
Podemos activarlo y no usar ningún template, lo dejamos como .None.
En mi sistema operativo no se puede ver esta subcarpeta pero está presente.

*EJEMPLO: Podemos ignorar todas las imágenes .jpg de la carpeta Ejemplos, solo escribe dentro de .gitignore lo siguiente:* 

```Ejemplos/*.jpg```

También yo siempre guardo las imágenes como: photo#.jpg donde # representa un número. Sí quisiera ocultar todas esas imágenes con un formato similar puedo usar *?* y lo siguiente:

```photo?.jpg``` 

**.gitignore y .git deben estar en el mismo directorio.** Ambas subcarpetas no las puedo ver con mi sistema operativo.

## CLASE 5

#### git tag

Agregar tags a commits específicos. Un tag es un labe,una etiqueta, etc.

#### git merge

Permite combinar diferentes cambios que se realizaron en diferentes ramas y unirlos.

#### git branch

Permite múltiples ramas en el desarrollo. Permite trabajar en paralelo en una rama respecto a la rama master.

#### git checkout

Permite cambiar entre diferentes ramas o tags.


# KEEP CODING!
![Imagen charla Mercado Libre en la UTN](https://github.com/cabustillo13/Git/blob/ramaSecundaria/Charla%20programacion%20en%20la%20UTN.jpeg)

