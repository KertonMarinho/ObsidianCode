
<h1 style="color:yellow">Fluxo de Trabalho</h1>
![[Pasted image 20230918213947.png|500]]
- <span style="color:orange">Add</span> adiciona mudanças ao index(arquivo temporário)
- <span style="color:orange">Commit</span> Passa as mudanças do index para o Head
- <span style="color:orange">push</span> Envia as mudanças ao repositório remoto(se houver)

---
# 1° passo - Git add
- adiciona as mudanças ao arquivo temporário Index
- Sintaxe: 

```shell
git add <arquivo>
git add*
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
# 3° passo - git push
- Envia as alterações do HEAD do repositório local para um repositório remoto
- Sintaxe:

```shell
git push origin master
git push origin funcionalidade_x