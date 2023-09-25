# instalando o git
- Entra no site 
	https://git-scm.com/download/
- verifica se o git foi instalado:
	- Windows+E, escreva cmd
```shell
git --version
```
---

<h2 style="color:orange">Configurando que está trabalhando na máquina atual  
</h2> 
```shell
git config --global user.name "kerton marinho"
```
----
<h2 style="color:orange">Configurando o email</h2>
```shell
git config --global user.email "kerton.marinho@outlook"
```
---
<h2 style="color:orange">Configurando o editor a qual está trabalhando</h2>
```shell
git ---global core.editor vscode
```

---
<h2 style="color:orange">Pega o nome ou o email que está cadastrado no git</h2>
```shell
git config user.name
git config user.email
```
---
<h2 style="color:yellow">Ler todas as informações</h2>
```shell
git config --list
```
---
<h2 style="color:red">Remover uma section no git</h2>
```shell
git config --global --remove-section-texto(palavra errada)
```

- Múltiplas contas do Git:
![[Múltiplas contas GIT no mesmo computador.pdf]]

---
