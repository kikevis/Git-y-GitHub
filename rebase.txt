# avancemos en master. Insertar "master 1" en historia.txt
$ git commit -am "Master 1"

# crear rama experimento
$ git branch experimento
$ git checkout experimento

# insertar "exp 1" en historia.txt
$ git commit -am "exp 1"
# insertar "exp 2" en historia.txt
$ git commit -am "exp 2"

# hecho lo anterior, vuelvo a master y sigo avanzando
$ git checkout master
$ git commit -am "Master 2"

# la base de la rama experimento esta un commit atras de master.
# hago primero rebase en experimento para que parezca que nacio en el ultimo commit de master y no en el penultimo
$ git checkout experimento
$ git rebase master

# ahora si la rama experimento parece haber nacido en el ultimo commit de master.
# puedo hacer rebase ahora pero a master, para integrar los cambios hechos en la rama experimento
$ git checkout master
$ git rebase experimento

# con lo anterior todos los cambios quedan como si se hubieran hecho linealmente en master.
# aparece primero el commit de master que le hacia falta a experimento
# aparecen luego los dos commits que habia hecho en experimento
# con lo anterior ya me sobra la rama experimento, asi que la borro
$ git branch -D experimento
$ git branch
$ git pull origin master
$ git push oorigin master