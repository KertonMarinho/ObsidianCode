# Instalando o git

<span style="color:yellow">Download</span>
<https://git-scm.com/>
<span style="color:yellow">Wndows</span>
<https://gitforwindows.org/>
<span style="color:yellow">Guia Prático</span>
<https://rogerdudler.github.io/gitguide/index.pt_BR.html>
# Verifica se o git foi instalado:
	
```shell
git --version
```

---
## Git config
- Define o usuário que irá trabalhar com o Git
- Para o usuário a nível de projeto cada projeto um nome retira ``--global``
- Sintaxe:

```shell
git config --global user.name "vinicius Borin"
```
## Girt config (alterar o email)
- Define o e-mail que irá trabalhar com o git
- Sintaxe:
```shell
git config --global user.email "vinicius@email.com"
```
## Git config (alterando editor padrão)
- Define o editor que irá trabalhar com o git
- Sintaxe:

```shell
git config --global core.editor notepad
```
## Git config (listar as configurações feitas)
- Listando as configurações
- Sintaxe:

```shell
git config --list
```

# Para pegar só o nome ou o email

```shell
git config --get user.name
ou
git config --get user.email
```

---
# Inicialização do repositório Git
- Pelo prompt de comando, entre na pasta do seu repositório
- Exemplo:

```shell
c:\users\vinicius\PychraProjects\pythonProject
```
- Inicia o projeto com git init
- Sintaxe:
```shell
git init
```
- Para verificar se tem Git no projeto ``git status``
	- se tiver on branch master siginifica que o Git já está iniciado:
	- ![[Pasted image 20230930103135.png]]
---
# Branchs (ramificações)
- Podemos ramificar nosso projeto para trabalharmos em funcionalidades separadas simultaneamente
- O Branch padrão é chamado de --master-- .
- É criado quando vc cria o repositório
# Merge
- Mescla branchs para juntar partes desenvolvidas

```
---
## Git log
- Apresenta o histórico de commits
- Sintaxe:

```shell
git log
```
---
## Git status
- Mostra os arquivos alterados e também os novos ainda não monitorados
- Sintaxe:

```shell
git status
```
---
## git branch
- Apresenta todos os branchs do projeto, bem como o que você está usando
- Sintaxe:
```shell
git branch
```
---
## Git reset
- Retorna a um estado anterior de commit 
- Sintaxe:
```shell
git reset --tipo <id_commit>
```
### tipos de reset
- <span style="color:aquamarine">soft</span> retorna imediatamente ao estado antes do commit
- <span style="color:aquamarine">Mixed</span> retorna ao estado antes do commit e antes do add
- <span style="color:aquamarine">hard</span> apaga tudo para antes do último commit (arquivos, alterações, tudo é apagado) 
- ---
## Git diff
- Mostra os detalhes das alterações nos arquivos
- Sintaxe:

```shell
git diff
git diff --name-only
git diff <nomeArquivo>
```
---
<h2 style="color:red">Remover uma section no git</h2>
```shell
git config --global --remove-section-texto(palavra errada)
```

- Múltiplas contas do Git:
![[Múltiplas contas GIT no mesmo computador.pdf]]
---
# manual do git
![[progit (1) 1.pdf]]