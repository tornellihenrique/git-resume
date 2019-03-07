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
 	 - Editado porem não colocado em imagem

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
