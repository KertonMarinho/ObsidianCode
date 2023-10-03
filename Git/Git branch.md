# Branchs (ramificações)
- Podemos ramificar nosso projeto para trabalharmos em funcionalidades separadas simultaneamente
- O Branch padrão é chamado de ``Main`` .
- É criado quando vc cria o repositório
- Para ver qual branch vc está

```shell
git branch
```

--- 
## Cria uma nova branch
- sintaxe:

```shell
git branch <nomeBranch>
```
---
# Ir para nova versão
- vc está na master:
![[Pasted image 20230930111616.png]]
- Para para ir para branch novaversão

```shell
git switch novaversao
```

![[Pasted image 20230930111814.png]]

---
## Git checkout
- Altera o branch atual de trabalho (escolha qual branch quer trabalhar)
- Sintaxe:

```shell
git checkout <nomeBranch>
```
- Podemos agora modificar o que quisermos dentro de outro branch, e  o master permanecerá intacto
---
# Branch de emergência
- Pega cria uma branch de emergência
```shell
git switch -c emergency-fix
//emergency-fit, nome sugerido
```
- depois de corrigir o bug, junto as duas branchs com ``merge``
---
# Juntar as branchs(git merge)
- Na master de o comando merge:
```shell
git merge <nome da brunch que que juntar com a master>
```
- Depois de juntar vc pode deletar a que foi juntada
- ele abre um editor de texto para que vc pode dizer porque vai juntar os aquivos
- ![[Pasted image 20230930130906.png|400]]
- ``ctrl + x`` - sai do editor
---
# Deletando brunch

```shell
git branch -d <nome da branch que quer deletar>
```
---
# Enviando alterações na branch intermediária
- vc pode fazer alteraçoes especificas na branch

```shell
git push origin main(branc mastare)
//ou
git push origin <nome da branc intermediária>
```
