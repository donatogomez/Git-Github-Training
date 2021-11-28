# Ejercicio 1

**¿Qué comando utilizaste en el paso 11? ¿Por qué?**<br>

`$ git reset --hard HEAD~1`

Este comando nos permite volver por completo al estado del *commit* anterior. El parámetro "*--hard*" descarta los cambios actuales del *working copy/tree*.

**¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**<br>

`$ git reflog`<br>
`$ git reset --hard e6d2290`

Con el comando "*git reflog*" podemos acceder a un registro que almacena todos los commits por donde pasó el puntero *HEAD*. Una vez ejecutado el comando, buscamos la posición a la que queremos volver. Una vez localizada copiaremos su *hashtag* para ejecutar el comando "*git reset --hard \<hashtag>*".

**El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**<br>
No. Es un merge fast-forward, al no haber ningún *commit* nuevo en la rama *master*, una vez creada la rama *styled*, no habrá conflictos. Al hacer el *merge*, *styled* absorbe los commits de *master*.

**El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?**<br>
Sí. Si una o más líneas de un mismo archivo son editadas en distintas ramas, cuando intentemos fusionarlas, git nos lanzará un aviso para que revisemos el contenido del mismo y mantengamos/descartemos lo que necesitemos. Una vez editado el fichero añadiremos los cambios al *staging area* y después al *repositorio*, para completar nuestro *merge*.

**El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**<br>
No hay conflictos. Este es un *merge fast-forward*. Cuando intentamos *mergear commits* cuyas ramas siguen la misma ruta, git nos simplifica el proceso moviendo el puntero  hasta el último *commit* de la rama que absorbe.

**¿Qué comando o comandos utilizaste en el paso 25?**<br>

`git log --graph --pretty=oneline`

Alternativamente podemos añadir un alias al comando para que cada vez que queramos consultar el grafo no tengamos que escribir todo el comando de nuevo.

`$ git config alias.graph “log --graph --pretty=oneline”`

**El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**<br>
Sí, porque solo hemos realizado nuevos *commits* en la rama *title*. Si no lo especificamos, git automáticamente nos hará un *merge fast-forward*.

**¿Qué comando o comandos utilizaste en el paso 27?**<br>

`$ git reset HEAD~1`

**¿Qué comando o comandos utilizaste en el paso 28?**<br>

`$ git restore git-nuestro.md`

**¿Qué comando o comandos utilizaste en el paso 29?**<br>

`$ git branch -D title`

Necesitamos forzar el borrado con el parámetro *-D*, ya que la rama *title* contiene trabajo sin *mergear*.

**¿Qué comando o comandos utilizaste en el paso 30?**<br>

`$ git reflog`<br>
`$ git reset --hard 3413c14`

**¿Qué comando o comandos usaste en el paso 32?**<br>

`$ git log`<br>
`$ git reset --hard 9932ecb79faf89464ff487339a8d89bc6944532f`

Al estar situados en la rama *master* que es donde hicimos el primer *commit* podemos hacer uso de "*git log*", alternativamente o si este no fuera el caso también podríamos hacer uso de "*git reflog*".

**¿Qué comando o comandos usaste en el punto 33?**<br>

`$ git reflog`<br>
`$ git reset --hard 187c5b4`
