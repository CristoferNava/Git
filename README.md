# Comandos importantes de Git

**git --version**: Muestra la versión de Git.

**git help**: Información general de Git.

**git help log**: Información de un comando en específico.

**git init**: Crea un repositorio local.

**git config --global user.name "name"**: Configurar nombre de usuario.

**git config --global user.email "e@m.com"**: Configurar email de usuario.

**git config --global -e**: Editar la configuración global de Git.

**git status**: Muestra el estado del repositorio, seguimientos y stage.

**git add .**: Añadir todo al stage.

**git commit -m "message"**: Crear snapshot del stage.

**git remote add origin url**: Acceso remoto al repositorio indicado.

**git remote -v**: Verbal del git remote.

**git remote add upstream url**: Crea una nueva fuente llamada upstream la cual está
vinculada con la url indicada.

**git pull upstream master**: Traemos todos los cambios de la rama upstream (fuente) a la
master.

**git push origin master**: Subimos los cambios de master al repositorio remoto origin.

**git checkout -- .** Reconstruye el repositorio a como se encontraba en el último commit.

**git log** Información de la línea del tiempo.

**git log -S "asterdots"**: Busca la palabra asterdots en los commits de la rama en la que nos
encontramos.

**git shortlog**: Muestra los commits que ha realizado cada persona.

**git log file.txt**: Información de la línea del tiempo de un archivo en particular.

**git reset archivo**: Remover archivo del stage.

**git add "*.txt"**: Agrega al stage todos los txt encontrados en TODO el repositorio.

**git add \*.txt**: Agrega al stage todos los txt del directorio actual.

**git config --global alias.lg "log --oneline --decorate --all --graph"**: Crea alias con el nombre de *lg*.

**git diff**: Muestra todas las modificaciones entre lo que está en el stage y lo que no.

**git diff hash1 hash2**: Compara los cambios de los dos commits (primero anterior, segundo nuevo).

**git diff --staged**: Verifica también los archivos que se encuentran en el stage.

**git checkout -- README.md**: Restaura el archivo a como se encontraba en el último commit.

**git commit --amend -m "Se corrigió el mensaje del commit"**: Fusiona los cambios actuales
con los del commit anterior.

**git reflog**: Historial completo del repositorio.

**git branch**: Muestra las ramas y señala en la que estamos ubicados.

**git branch -r**: Muestra las ramas remotas.

**git branch -a**: Muestrea todas las ramas, locales y remotas.

**git branch branch-name**: Crea una nueva rama.

**git checkout branch-name**: Nos cambia a la rama indicada.

**git diff branch1 branch2**: Diferencias entre branch1 y branch2.

**git merge branch1**: Une branch1 a la rama en la que nos encontramos actualmente.
Es necesario poner un mensaje explicando porque hicimos este merge.

**git branch -d branch1**: Borra la branch1.

**git checkout -b branch1**: Crea una nueva rama y nos cambia a ella.

**git show-branch --all**: Muestra información importante de las ramas.

**git push origin branch**: origin hace referencia al repositorio remoto y branch 
al nombre de la rama que se le va hacer push.

**git show file.txt**: Información útil de los cambios realizados.
<hr>

## Viajando en el tiempo
**git checkout hash file.txt**: Nos movemos a como estaba el archivo en el commit 
indicado. (Revisar si queremos guardar o no las modificaciones).

**git reset hash**: (Cuidado) Volvemos en el tiempo pero también borramos la historia
después del hash. Volvemos al pasado pero no podemos regresar al futuro.

**git reset hash --hard**: (Cuidado) Volvemos en el tiempo y borramos toda la información
que tengamos en el stage.

**git restet hash --soft**: (Cuidado) Volvemos el el tiempo pero mantenemos la 
información del stage la cual será guardada pero desde el hash.
<hr>

## Problemas con el pull
**git pull origin master --allow-unrelated-histories**: fatal: refusing to merge
unrelated histories.
<hr>

## Tags para releases
**git tag -a tag-name -m "Lista primera versión del proyecto" hash**: Coloca un tag
en el hash indicado.

**git tag**: Mostrar todos los tags.

**git show-ref --tags**: Mostrar más información de los tags.

**git tag -d tag-name**: Eliminar tag del repositorio local (luego comando de abajo).

**git push origin :refs/tags/tag-name**: Eliminar el tag del repositorio remoto (primero ejecutar comando
de arriba).

**git push origin --tags**: Enviamos los tags al repositorio remoto.
<hr>

## Para cambiar de rama sin tener que hacer commit de los cambios actuales
**git stash**: Ponemos los cambios en el stash.

**git checkout branch-name**: Nos movemos a la rama a la que queremos revisar y 
luego regresamos a la rama original haciendo de nuevo checkout.

**git stash pop**: Sacamos los cambios que habiamos dejado en el stash.

**git stash list**: El stash es un lugar temporal para guardar los cambiamos, con
list podemos listar lo que en él se encuentre.

**git stash branch branch-name**: Poner el stash en la rama indicada.

**git stash drop**: Vacía el stash.
<hr>

## Para casos de emergencia (tener cuidado, es una mala práctica, último recurso)
Si todo sale mal y necesitamos volver en el tiempo a donde todo estaba cool

**git reflog**: Muestra toda la historia del repositorio.

**git reset --hard hash**: Nos regresa a como estábamos en ese commit.

**git reset --soft hash**: La diferencia entre soft y hard es que el primero mantiene
los cambios del stage y hard los elimina.