# Taller de Git
## Principales comandos
### Cristofer Nava

**git --version** Versión de Git.

**git help** Información general de Git.

**git help** ***commit*** Información de un comando en específico.

**git init** Crea un repositorio local.

**git config --global user.name "name"**

**git config --global user.email "e@m.com"**

**git config --global -e**

**git init** Crear nuevo repositorio.

**git status** Muestra el estado del repositorio.

**git add .** Añadir todo al stage.

**git commit -m "message"** Crear snapshot del stage.

**git checkout -- .** Reconstruye el repositorio a como se encontraba en el último commit.

**git log** Información de la línea del tiempo.

**git log file.txt** Información de la línea del tiempo de un archivo en particular.

**git reset archivo** Remover archivo del stage.

**git add "*.txt"** Agrega al stage todos los txt encontrados en TODO el repositorio.

**git add *.txt** Agrega al stage todos los txt del directorio actual.

**git config --global alias.lg "log --oneline --decorate --all --graph"**: Crear alias con el nombre de *lg*.

**git diff**: Muestra todas las modificaciones entre el commit anterior y el momento actual.

**git diff --staged**: Verifica también los archivos que se encuentran en el stage.

**git checkout -- README.md** Restaura el archivo a como se encontraba en el último commit.

**git commit --amend -m "Se corrigió el mensaje del commit"**

***HEAD***: Apunta al último commit.

***HEAD^***: Apunta el penúltimo commit.

**git reset --soft HEAD^**: Juntar cambios actuales con el commit anterior.

**git reset --soft *hash***

**git reset --mixed *hash***

**git reset --hard *hash***

**git reflog**: Historial completo del repositorio.