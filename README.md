# GIT E GITHUB

## CONFIGURAÇÕES BÁSICAS

- Definir nome global
```sh
git config --global user.name "Nome Completo"
```
- Definir email global
```sh
git config --global user.email "email@email.com"
```
- Definir editor global
```sh
git config --global core.editor ${editor command}
```
- Verificar as info globais
```sh
git config user.${param}
git config --list
```
-------------------------------------------------
## ESTADOS

- UNTRACKED
 	 - Não visto pelo Git

- UNMODIFIED
 	 - Sem modificação

- MODIFIED
 	 - Editado porem não adicionado ao _stage_

- STAGED
 	 - Pronto para ser commitado

-------------------------------------------------

## REPOSITÓRIO

- Inicializar repositório
```sh
git init
```
- Verificar o status
```sh
git status
```
- Verificar mudanças
```sh
git diff
	--name-only (somente nomes de arquivos)
```
- Adicionar diretório ou arquivo
```sh
git add ${dir/file}
```
- Commitar arquivos adicionados
```sh
git commit -m "${Comment}"
```
- Adicionar e commitar diretório atual (git add .)
```sh
git commit -am "${Comment}"
```
- Adicionar repositório remoto
```sh
git remote add _origin_ ${git link}
```
- Verificar o repositório
```sh
git remote
	-v (verifica endereço)
```
- Enviar o repositório local para remoto (inicial)
```sh
git push -u origin master
```
- Envia o repositório local para remoto
```sh
git push
```
- Verificar log
```sh
git log 
	--decorate (info adicionais) 
	--author="${author}" (filtro por autor)
	--graph (forma grafica de branchs)
```
- Log em ordem alfabética por autores
```sh
git shortlog
	-sn (autores e numero de commits)
```
- Informações de algum commit
```sh
git show ${commit hash}
```

## Branchs, Merge e Rebase
- Cria uma branch
```sh
git checkout -b ${name}
```
- Lista as branchs
```sh
git branch
```
- Navega entre banchs
```sh
git checkout ${branch}
```
- Deleta alguma branch local
```sh
git branch -D ${branch}
```
- Deleta alguma branch remota
```sh
git push origin :${branch}
```
- Faz um merge para a branch atual
```sh
git merge ${branch}
```
- Faz um rebase para a branch atual
```sh
git rebase ${branch}
```

## Desfazendo alterações
- Retornar dir/arq para antes da edição (não adicionado)
```sh
git checkout ${dir/file}
```
- Remover alterações da fila de adições (add)
```sh
git reset HEAD ${dir/file}
```
- Desfazer commits
```sh
git reset
	--soft ${commit hash} (Desfaz o commit para aquela hash)
	--mixed ${commit hash} (Desfaz o commit e o add para aquela hash)
	--hard ${commit hash} (Desfaz o commit, o add e as alterações feitas para aquela hash)
```
- Desfaz o ultimo commit sem perder o codigo local com um novo commit
```sh
git revert ${commit}
```
## Extras
#### Stash
- Guarda as modificações no stash
```sh
git stash
```
- Lista as modificações no stash
```sh
git stash list
```
- Aplica as modificações no stash
```sh
git stash apply
```
- Limpa as modificações guardadas no stash
```sh
git stash clear
```
### Alias
- Cria um atalho de comando
```sh
git config --global alias.${alias} ${alias command}
```
### Tags
- Cria uma tag no commit e branch atuais
```sh
git tag -a ${version} -m ${comment}
```
- Envia o push com a tag
```sh
git push origin master --tags
```
- Apaga a tag local
```sh
git tag -d ${tag}
```
- Apaga a tag remota
```sg
git push origin :${tag}
```
