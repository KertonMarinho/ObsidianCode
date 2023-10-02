1. Cria o repositório no github:
![[Pasted image 20231001213214.png|300]]
2. No terminal, entre na pastas do projeto, de o comando para clonar o projeto do githbu com o local

```shell
git clone <endereço do site do projeto>
```
- ele cria um repositório local com o  mesmo nome do github
- no git status,ela mostra que a branch está atualizada com o origin/main

![[Pasted image 20231001214531.png]]

---
# Sincronizando com ssh
- Segue os passos do tutorial do gi ou mande estes comandos:
```shell
echo "# <nome do repositório>"
git init
git add Readme.md
git commit -m "first commit"
git remote add origin <endereço de repositório>
git push -u origin maste
```

---
# se já existe o repositório no gitHub já criado de estes comandos

```shell
git remote add origin <endereço de repositório no github>
git push -u origin master
```

>[!warning]
>estes comandos é usado somente na primeira vez
