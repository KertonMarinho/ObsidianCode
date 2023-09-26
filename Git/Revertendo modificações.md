# Git reset (três formas)

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
