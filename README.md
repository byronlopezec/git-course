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
git checkout -- .  # reconstruye el proyecto a como estaba el ultimo commit
git reset --soft HEAD^1 # regresar a un commit anterior