# git-course

git init 			# crear repositorio
git commit -am "agrega archivos "
git reset <archivoQueNoQueremosIngresarAlcommit> #desacer cambios o quitar del precommit
git config core.autocrlf true # eliminar mensaje de LB wil be replaced by CRLF
git config --global -e # abre el archivo .gitconfig para editar
git config --global alias.s "status --short:" # agregar un alias, se invocaría así: git s
git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all" # alias muy bueno para ver logs
git commit --amend -m "modifica el titulo del anterior commit"
git commit --amend --no-edit # util para agregar archivos olvidados de agregar al anterior commit
git diff # ver cambios de mi version
git checkout -- .  # reconstruye el proyecto a como estaba el ultimo commit, conserva nuevos archivos pero no cambios
git reset --soft HEAD^1 # regresar a un commit anterior sin destruir actuales cambios 
git reset --soft ea8cc70 # regresar a un commit ea8cc70 sin destruir los actuales cambios
git reset --mixed ea8cc70 # regresar al commit ea8cc70 sin destruir cambios pero similar a soft 
git reset --hard <idcommit> #ir al commit idcommit y destuir cualquier cambio actual del stage.
git reset --hard # similar git checkout -- . para restablecer destruyendo cambios del stage
git reflog # lista los commit realizados en order
git checkout -b <nuevaRama> # crea y se posiciona en la nueva Rama

git branch -d <nombreRama> # eliminar rama local
git branch -d <nombreRama> - f # -f para forzar la eliminacion 
// merge
fast-forward -- union sin conflictos
recursive -- se hace commits en master pero tambien se hacen commits en la nueva rama
