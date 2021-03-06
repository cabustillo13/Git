# GIT COMANDOS

## FUNDAMENTAL

**Problemas con fastforward**

Cuando tenga problemas con un merge debido a un fastforward.

```
git commit -a -m "Razón de cómo arregle este problema"
git pull
```
Ahora se verifica sí localmente tengo cambios.

```
git status
git push
```
**Mantener actualizados mis forks con la el proyecto original**

Cuando quiero mantener sincronizado un fork actualizado con el proyecto orginal puedo consultar la siguiente página: [Ver](https://victorhckinthefreeworld.com/2016/12/14/git-mantener-un-fork-de-un-repositorio-actualizado/). Recordar que actualiza todo localmente, después de hacer el último paso se debe hacer un git commit y git push.

```
git checkout master
git merge upstream/master
git commit -m "Mensaje para mi proyecto"
git push
```

**Hacer un git push desde mi fork al proyecto original**

```
git add .
git commit -m "Add mensaje"
git push origin ramaSecundaria
```

## CLASE 1

* **Crear un .md desde terminal y para luego hacerle un push**
```
echo "# Git" >> README.md
git init

git add README.md
git push
```
## CLASE 2

* **Crear un nuevo repositorio, vacío y en la carpeta donde estamos parados localmente**

```git init```
## CLASE 3

* **Conocer quién y cuándo se realizaron los commits**

```git log```

![Resultado](https://github.com/cabustillo13/Git/blob/master/git%20log.png)

Ahí solo nos muestra los SHA recientes. Sí queremos seguir bajando apretamos en el teclado **j** y si queremos subir **k**. 
También se puede hacer con las flechas de arriba y abajo.

Para salir solo apreto **q**.

```git log SHA```

Colocas el *SHA* del commit que estás buscando. No gace falta escribir todo el SHA, con 6-8 carácteres es suficiente.

```git log --oneline```

Acá directamente me devuelve solo el título del mensaje junto a su respectivo SHA.

![git log --oneline](https://github.com/cabustillo13/Git/blob/master/git%20log%20--oneline.png)

Para salir solo apreto **q**.

*CUIDADO: Un error de noob es escribir "online", en vez de "oneline".*

```git log --stat```

Devuelve los tipos de cambios que se realizaron para commit.

![git log --stat](https://github.com/cabustillo13/Git/blob/master/git%20log%20--stat.png)

```git log --stat SHA```

Sí quiero obtener directamente los cambios que se le hicieron directamente a un commit, le agrego su SHA.

```git log -p```

Muestra qué líneas de código fueron modificadas y qué fue lo que se modificó para commit.

![git log -p](https://github.com/cabustillo13/Git/blob/master/git%20log%20-p.png)

Las líneas color verde fue lo que se añadio y las de color rojo las que se eliminaron.

Y la parte que tiene @@ en cuáes líneas de código se realizaron los cambios. 
En la imagen que añadimos podríamos interpretarlo como: en la línea 38 se realizaron los cambios.

También puedo unir comandos como:

```
git log -p --stat
git log --stat -p
```
En ambos casos me devuelven lo mismo. 

```git log -p -w```

Ignora los espacios en blanco al comparar líneas. 
Osea hace lo mismo que ```git log -p``` pero sin resaltar las líneas donde solo se han producido cambios en los espacios en blanco.

```git show SHA```

Devuelve la información solo de un commit. 

Antes con ```git log SHA``` me devolvía primero la información del SHA que quería, y después mandaba información de todos los demás commits.

![git show SHA](https://github.com/cabustillo13/Git/blob/master/git%20show%20SHA.png)

También podemos agregarle -p -w --stat como en ```git log```

## CLASE 4

```git add carpeta1/archivo1.py```

Solo sube el archivo1.py que está dentro de la carpeta llamada "carpeta1".

```git add capeta1/archivo1.py imagenes/archivo2.cpp carpeta3/archivo3.py```

Solo añade los archivos: archivo1.py que está en la carpeta carpeta1, archivo2.cpp que está en la carpeta imágenes 
y archivo3.py que está en la carpeta carpeta3.

```git add .```

Añade todos los archivos nuevos que hemos creado y/o modificado.

```git commit```

Realiza un commit.

```git commit -m "Mensaje"```

Al agregarle ```-m``` permite agregarle un mensaje al commit.

*CONSEJO: **El objetivo es que cada commit tenga un solo enfoque.** Cada commit debe registrar un cambio de una sola unidad. Ahora, esto puede ser un poco subjetivo (lo cual está totalmente bien), pero cada commit debe hacer un cambio en solo un aspecto del proyecto*

*EJEMPLO:*
* *add a new image to the project files*
* *alter the HTML* 
* *add/modify CSS to incorporate the new image*

_**¡Aunque también, un commit que registra todos estos cambios estaría totalmente bien!**_

*Por el contrario, un commit no debe incluir cambios no relacionados entre sí: tipo cambios en la barra lateral y reescritura de contenido en el pie de página. Estos dos no están relacionados entre sí y no deben incluirse en el mismo commit. Primero trabaje en un cambio, comprométalo y luego cambie el segundo. De esa manera, si resulta que un cambio tenía un error y tienes que deshacerlo, no tienes que deshacer el otro cambio también.*

_La mejor forma en que he encontrado para pensar sobre lo que debería estar en un commit es pensar: **'¿Qué pasa si se borran todos los cambios introducidos en este commit?'**. Si se borra un commit, solo debería eliminar una cosa._

_DATO: Las líneas que comienzan con # son comentarios y no se registrarán._
*Tipo:* ```git commit -m "#Esto es un comentario"```. Aunque para usar eso, mejor uso solo ```git commit```.

## CLASE 5

```git tag -a version1.0 -m "Mensaje"```

```git tag -a Beta -m "Mensaje"```
 
Permite agregarle etiquetas a commits específico. Reemplazar ```Mensaje```, por el mensaje del commit.Lo puedo usar cuando suba una nueva versión. *EJEMPLO: Como cuando en mi sudoku cuando le agrege una interfaz gráfica, a ese le pude poner un tag para marcar un antes y un después.*
 
*IMPORTANTE: No olvidar ponerle ```-a```, ésto le dice a Git que cree una flag anotada. Sí no se lo coloco se crea una "tag ligero".* 
*Una de las ventajas que tiene usarlo es que te permite ver: el mensaje, quién y cuándo se hizó. *

```git tag```

Retorna todos los tags que se han creado en el repositorio.

```git tag -d NombreTag```

Permite borrar un tag. Reemplazar ```NombreTag``` por el nombre del tag que se quiere eliminar.

```git tag -a NombreTag SHA -m "Mensaje"```

Permite agregrarle un tag a un commit que ya hemos subido. ```NombreTag``` por el nombre del tag con el que se quiere nombrar.

```git branch nombreRama```

Permite crear una rama nueva. Escribir nombre en la rama en ```nombreRama```.

```git branch```

Permite visualizar todas las ramas creadas.

```git push --set-upstream origin nombreRama```

Permite cargar mi rama que cree desde la consola.

```git checkout nombreRama```

*EJEMPLO: Sí escribo ```git branch nombreRama SHA``` va a crear la rama nombreRama y va a apuntar a ese SHA.*

Permite cambiar la rama donde estoy parado, y apuntar a ```nombreRama```. 

```git branch -d nombreRama```

Borra la rama nombreRama.

**Una cosa a tener en cuenta es que NO puede eliminar una rama en la que se encuentra actualmente.** Para eso, me muevo a la rama master y 
borro desde ahí la rama nombreRama. 

```git branch -D nombreRama```

Borrar forzosamente nombreRama, sí es que Git no me dejama borrarla por algún inconveniente con ```-d```.

```git checkout -b nombreRama```

Permite crear una nueva rama nombreRama y pararse en esa nueva rama creada en un solo paso.

```git log --oneline --graph --all```

```--graph``` agrega las viñetas y líneas a la parte más a la izquierda de la salida. Esto muestra la ramificación real que está sucediendo. 
```--all``` es lo que muestra todas las ramas en el repositorio.

![Imagen git log --oneline --graph --all](https://github.com/cabustillo13/Git/blob/ramaSecundaria/git%20log%20--oneline%20--graph%20--all.png)

## IMPORTANTE

```git reset --hard HEAD^```

Sí alguna vez haces un merge con la rama equivocada, puedes deshacerlo con ese comando.

**Hay que asegurarse de incluir el carácter ```^``` Se conoce como una 'Referencia de confirmación relativa' e indica 'la confirmación principal'.**

```git merge nombreRama -m "Mensaje"```

Primero debo asegurarme de que estoy parado en la rama master. Luego ejecuto ese comando para hacer un merge de nombreRama a la rama master. 
También puedo hacer merge entre ramas si quiero.

![Imagen de un merge de ramaSecundaria a la rama master](https://github.com/cabustillo13/Git/blob/master/git%20merge.png)

En la imagen se puede apreciar un merge de la ramaSecundaria a la rama master.

## CLASE 6

```
git add .
git commit --amend
```

_EJEMPLO: Olvidaste agregar algo, recortar una imagen, colocar un título, etc_

```git revert SHA```

Lo que hace es que a partir de ese ```SHA```, todos los commits poteriores a ese los elimina.

# KEEP CODING!
![Imagen charla Mercado Libre en la UTN](https://github.com/cabustillo13/Git/blob/ramaSecundaria/Charla%20programacion%20en%20la%20UTN.jpeg)




