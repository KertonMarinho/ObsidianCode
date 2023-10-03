1. Acesse [CLI do GitHub | Leve o GitHub para a linha de comando](https://cli.github.com/)
2. Para checar a versão

```shell
gh --version
```

3. Faça o login por meio do CLI

```shell
gh auth login
```

4. escolhe a conta github.com
---
# via https:

5. escolhe com HTTPS
6. ele pergunta que vc quer autenticar a suas credenciais com github, sim
7. Como vc que autenticar pelo Cli ,escolhe browser ou token
8. escolha navegador e copie o código
![[Pasted image 20231001223548.png]]
9. De enter e abre o navegador
10.digite o código
11. aperte o botão ``authorize github``
12. vai pedir um código de autenticação dois fatores
13. no terminal mostrar que teve autenticação completa
---
# via Token
5. No github crie o token
	- settings>deveolper settings>personal access tokens>token(classic)>canto direito superior>generate new token>generate new token(classic)>nome do token:token-exemplo
	- pode especificar data de expiração do token:``experitation``
6. ele pergunta que vc quer autenticar a suas credenciais com github, sim
7. colando o token de auteticaçao
8. forneça o token,enter