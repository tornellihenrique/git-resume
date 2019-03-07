# GIT E GITHUB

 > CONFIGURAÇÕES BÁSICAS

- Definir nome global
git config --global user.name "Nome Completo"

- Definir email global
git config --global user.email "email@email.com"

- Definir editor global
git config --global core.editor code

- Verificar as info globais
git config user.${param}
git config --list

-------------------------------------------------
 > ESTADOS

 1 UNTRACKED
 	 - Não visto pelo Git

 2 UNMODIFIED
 	 - Sem modificação

 3 MODIFIED
 	 - Editado porem não colocado em imagem
 
 4 STAGED
 	 - Pronto para ser commitado

-------------------------------------------------

 > REPOSITÓRIO

- Inicializar repositório
 git init

- Verificar o status
git status

- Verificar mudanças
git diff
	--name-only (somente nomes de arquivos)

- Adicionar diretório ou arquivo
git add ${dir/file}

- Commitar arquivos adicionados
git commit -m "${Comment}"

- Adicionar e commitar diretório atual (git add .)
git commit -am "${Comment}"

- Verificar log
git log 
	--decorate (info adicionais) 
	--author="${author}" (filtro por autor)
	--graph (forma grafica de branchs)

- Log em ordem alfabética por autores
git shortlog
	-sn (autores e numero de commits)

- Informações de algum commit
git show ${commit hash}

- Retornar dir/arq para antes da edição (não adicionado)
git checkout ${dir/file}

- Remover alterações da fila de adições (add)
git reset HEAD ${dir/file}

- Desfazer commits
git reset
	--soft ${commit hash} (Desfaz o commit para aquela hash)
	--mixed ${commit hash} (Desfaz o commit e o add para aquela hash)
	--hard ${commit hash} (Desfaz o commit, o add e as alterações feitas para aquela hash)
