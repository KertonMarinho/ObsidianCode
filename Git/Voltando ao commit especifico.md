- Cuidado vc pode perder o commit
- Revertendo modificações
---
# Git Revert
- Pega o commit anterior e mantém o Histórico de modificações do anterior
-  reverte para o arquivo anterior, ainda tem acesso ao commit que ocorreu o erro
- O commit com erro não é apagado
- para voltat o commit com defeito, git reset
```shell
git revert <códgo-do-commit-com problema>
```
ou vc pode usar o ``Head``
```shell
git revert HEAD
```
- Vc pode especificar uma mensagens para especificar o commit novo
```shell
git revert HEAD -m "mensagens"
```
- ou pode pode colocar o commit com o nome revert:

```shell
git revert HEAD --no-edit
```

	![[Pasted image 20230930122927.png]]
	 ``Revert + o nome do commit que reverteu``

---
# Git Reset
- Não use se outro desenvolvedor tiver trabalhando no mesmo repositório

```shell
git reset <numero do log>
```
- Ele volta para o histórico mais ele não alterou os arquivos
# Git Stash
- ele ignorar qualquer alterações que não foi alterada ainda depois do git reset
- Use depois do Git Reset
- exemplo, ele vai ignorar que vc deletou o ``.gitigonre``
![[Pasted image 20230930124530.png|500]]

```shelll
git stash
```
- v pode com ``stash`` alterar antes o commit para o estagio inicial sem mesmo fazer o commit
- Exemplo, modificou o arquivo no vscode e antes de fazer qualquer coisa no terminal , vc pode voltar ao estagio do começo do código usando ``stash``

---
# Revertando modificacões de três formas diferentes
``uninter,desenvolvimento de sistemas``

<h1 style="color:yellow">Soft</h1>
- Volta para o commit desejado
- mas com alterações  de modificações resetadas não commitadas

```shell
git reset --soft <numero do commit que deseja voltar>
```
---
<h1 style="color:yellow">Mixed</h1>
- Volta para o commit desejado
- mas terá que adicionar para monitorar os arquivos adicionados
- continua com alterações sem commitadas

```shell
git reset --mixed <numero do commit que deseja voltar>
```
---
<h1 style="color:yellow">Hard</h1>
- Apaga todas as modificações
- volta para as versões do commit desejado
- Não recomendado quando você tem equipes do projeto

```shell
git reset --hard <numero do commit que deseja voltar>
```

---
>[!warning]
>A principal diferença entre o git revert e o git reset é a abordagem para desfazer alterações. O git reset desfaz um ou mais commits descartando-os completamente, o que pode levar a uma perda permanente das alterações feitas nesses commits.   
>O uso do git revert é recomendado quando você está trabalhando em um ambiente colaborativo, onde outros membros da equipe podem ter se baseado nos commits anteriores. O git revert permite desfazer alterações de forma segura, preservando o histórico e evitando possíveis conflitos com outros desenvolvedores.  
  Em resumo, o git revert é útil para desfazer alterações de forma segura e manter o histórico consistente, enquanto o git reset é mais adequado para redefinir o estado do repositório de forma mais drástica, descartando alterações não desejadas. A escolha entre eles dependerá das necessidades do seu projeto e das circunstâncias específicas.
  