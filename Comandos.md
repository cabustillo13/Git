# Git

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
*Tipo:* ```git clone -m "#Esto es un comentario"```
