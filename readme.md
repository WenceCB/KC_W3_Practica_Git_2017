## PRÁCTICA GIT

 
11.- Deshacer el último commit (perdiendo los cambios realizados 
en 	el working copy)

>	¿Qué comando utilizaste en el paso 11? ¿Por qué?
	
>>		
		git reset --hard HEAD~1
		
> He utlizado hard ya que se nos pide que se descarten los cambios y dicho comando además de mover el puntero Head reestablece el working copy al punto en el que se encontraba en ese momento	


12.- Rehacer el último commit ( el que acabamos de hacer )

> ¿Qué comando utilizaste en el paso 12?, ¿Por qué?

>>		   git reflog
		git checkout <HASH>
		git branch <RAMA>

>    Aquí podría utilizar dos comandos , o bien un git reflog para
		ver en que posición está el commit al que queremos ir
		y posteriormente con checkout movernos a 
		la rama correspondiente o hacer un git reset
		utilzando el hash, en este	caso he usado un git
		checkout al commit y después me he movido a la rama htmlify
		

13.- Hacer un merge con 'master'  ( styled absorve a master )

> El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
>>		   git branch
		git merge master
> En primer lugar compruebo que estoy posicionado en la rama
 que va a absorber a master , a continuación realizo el merge. En este caso no hay conflicto porque la rama htmlify tiene acceso a master ( es lineal ) por lo tanto hacer un merge o no van a tener el mismo acceso al primer commit que es dónde está alojado **git-nuestro.md**
 

19.- Hacer un merge "htmlify" en "styled" (styled absorbe a htmlify)
>El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
>>		   git branch
		git merge htmlify
>Compruebo en la rama que estoy (styled) y posteriormente hago el merge , no ha habido ningún problema y en este caso el merge ha sido **Fast-Foward**

21.- Desde "master" , hacer un merge con "styled"
>El merge dle paso 21, ¿Causó algún conflicto? ¿Por qué?
>>		   git checkout master
		git merge styled
>Se hace el merge sin problemas , al igual que el anterior **Fast-Foward**

25.- Dibuja el diagrama
>¿Qué comandos utilizaste en el paso 25?
>> 		$ git log --graph --abbrev-commit --decorate --all
>>	![captura](graph.tiff)


26.- Hacer un merge “no fast-forward” de “title” en “master” (master absorbe a title) 
>El merge del paso 26 , ¿Podría ser **Fast-Foward**?
>> 		git merge --no-ff title
>Si fuese fast foward desplazaríamos el puntero master al commit de title , en este caso title se mantiene en su commit y tanto **master** como **HEAD** se depslazan juntos al commit de la uníon

27.-Deshacer el merge ( sin perder los cambios del working copy)
>¿Qué comando o comandos utilizaste en el paso 27?
>>		git reset HEAD~1
>Volvemos atrás sin descartar los cambios del Working copy

28.-Descartar los cambios
>¿Qué comando o comandos utilizaste en el paso 28?
>>		git checkout git-nuestro.md

29.- Eliminar la rama "title"
>¿Qué comando o comandos utilizaste en el paso 29?
>>			git branch -D title
> Aunque haya borrado la rama el contenido del working copy y staying area no varía dado a que hemos eliminado un puntero del grafo

30.- Rehacer el merge que hemos deshecho
>¿Qué comando o comandos utilizaste en el paso 30?
>>		   git reflog
		git checkout (Hash)
> Comprobamos la posición del commit antes de borrar , y después nos movemos hasta él		

32.- Volver al commit inicial cuando se creó el poema
>¿Qué comando o comandos utilizaste en el paso 32?
>>		   git reflog
		git checkout (Hash) / git reset (Hash)
>Comprobamos la posición del commit antes de borrar , y después nos movemos hasta él			

33.- Volver al estado final, cuando pusimos título al poema
>¿Qué comando o comandos utilizaste en el paso 33?
>>		   git reflog
		git checkout (Hash) / git reset (Hash)
>Comprobamos la posición del commit antes de borrar , y después nos movemos hasta él	