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

Ahí solo nos muestra los SHA recientes. Sí queremos seguir bajando apretamos **j** y si queremos subir **k**. 
También se puede hacer con las flechas de arriba y abajo.

Para salir solo apreto **q**.

```git log SHA```

Colocas el *SHA* del commit que estás buscando. No gace falta escribir todo el SHA, con 6-8 carácteres es suficiente.

```git log mensaje```

Colocas en *mensaje* el título con que nombraste tu commit.

*EJEMPLO: Yo en algún momemento hice un git commit -m "título del mensaje". Bueno yo puedo buscar ese título del mensaje con git log.*
