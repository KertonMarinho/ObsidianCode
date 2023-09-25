
<h1 style="color:yellow">Fluxo de Trabalho</h1>
![[Pasted image 20230918213947.png|500]]
- <span style="color:orange">Add</span> adiciona mudanças ao index(arquivo temporário)
- <span style="color:orange">Commit</span> Passa as mudanças do index para o Head
- <span style="color:orange">push</span> Envia as mudanças ao repositório remoto(se houver)

---
# 1° passo -Entra n pasta do projeto

```shell
cd <pasta do projeto>
```
----
# 2° passo - Git add
- adiciona as mudanças ao arquivo temporário Index
- Sintaxe: 

```shell
git add -A
// (*) primeiro commit adcione tudo
```
---
# 2° passo - git commit
- Confirma as mudanças, gravando permanente no arquivo HEAD do repositório
- Sintaxe:

```shell
git commit -m "comente suas modificações"
```
---
# 3°passo - Cria um nove repositório gitHub
- em New repositório
> [!SUMMARY] Initialize this repositório
> Add a radme file - Adicione automaticamente o README
> ADD .gitignore - ignore alguns arquivos
> Chose a license -  escolhe o tipo de licença

- Siga os passos do tutorial do github
# 3° passo - git push
- Passe do repositório origin(local) para master(remoto)
- Sintaxe:

```shell
git push -u origin main
