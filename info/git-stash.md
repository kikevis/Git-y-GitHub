## Stash

git stash : Guarda el trabajo actual de manera temporal. (Archivos modificados o eliminados)

git stash -u : Crea un stash con todos los archivos. (Añadiendo los creados Untracked)

git stash save “mensaje” : Crea un stash con el mensaje especificado.

git stash list : Permite visualizar todos los stash existentes.

git stash clear : Elimina todos los stash existentes.

git stash drop : Elimina el stash más reciente. El que tiene num_stash=0.

git stash drop stash@{num_stash} : Elimina un stash específico.

git stash apply : Aplica el stash más reciente. El que tiene num_stash=0.

git stash apply stash@{num_stash} : Aplica los cambios de un stash específico.

git stash pop : Aplica el stash más reciente y lo elimina. El que tiene num_stash=0.

git stash pop stash@{num_stash} : Aplica los cambios de un stash específico y elimina lo stash.

git stash branch nombre_de_rama : Crea una rama y aplica el stash mas reciente.

git stash branch nombre_de_rama stash@{num_stash} : Crea una rama y aplica el stash especificado.

## Consideraciones:
El cambio más reciente (al crear un stash) SIEMPRE recibe el valor 0 y los que estaban antes aumentan su valor.
Al crear un stash tomará los archivos que han sido modificados y eliminados. Para que tome un archivo creado es necesario agregarlo al Staging Area con git add [nombre_archivo] con la intención de que git tenga un seguimiento de ese archivo, o también utilizando el comando git stash -u.
Al aplicar un stash este no se elimina, es buena práctica eliminarlo.