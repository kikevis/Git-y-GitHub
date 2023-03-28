## Ramas
git branch

git show-branch

git show-branch --all

git branch nombre-rama //crear rama

git checkout -b nombre-rama //crea e ingresa a la rama creada

git branch -d nombre rama //borrar rama

git push origin nombre-rama //envia rama al repositorio

gitk //mirar historial de las ramas de manera visual

git checkout nombre-rama //cambiar de rama

Las ramas son la forma de hacer cambios en nuestro proyecto sin afectar el flujo de trabajo de la rama principal. Esto porque queremos trabajar una parte muy específica de la aplicación o simplemente experimentar.

git branch -nombre de la rama-: Con este comando se crea una nueva rama.

git checkout -nombre de la rama-: Con este comando puedes saltar de una rama a otra.

git checkout -b rama: Crea una rama y nos mueve a ella automáticamente, Es decir, es la combinación de git brach y git checkout al mismo tiempo.

git reset id-commit: Nos lleva a cualquier commit no importa la rama, ya que identificamos el id del tag., eliminando el historial de los commit posteriores al tag seleccionado.

git checkout rama-o-id-commit: Nos lleva a cualquier commit sin borrar los commit posteriores al tag seleccionado.