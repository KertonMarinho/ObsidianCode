  
Variáveis de ambiente no Node.js são variáveis acessíveis globalmente no ambiente do sistema operacional. Elas são configuradas fora da aplicação e podem ser acessadas por qualquer processo em execução no sistema.

1. cria uma ``arquivo``fora do src, junto com package para guardar as variáveis de ambiente ``.env``
- neste arquivo se guarda qualquer informação para o sistema inteiro tem acesso 
- No github ele ignora este arquivo
- Este arquivo guarda infromações do  do ambiente

2. Como exemplo digite uma porta neste arquivo
	- Geralmente os nomes da variáveis de ambiente coloque os nomes todos maíusculo
![[Pasted image 20240105230829.png]]
3. No CMD instale o ``dotenv``
```shell
c:\projetos\node-mod1> mpm install dotenv
```

4. importar a função <u>dotenv</u> no arquivo``server.ts
```ts
import dotenv from 'dotenv';
```
5. chama a função agora no arquivo`` server.ts``
```ts
dotenv.config(); //agora o sistema tem acesso as variáveis de ambiente
```
6. Para seu uso no arquivo ``server.ts``
```ts
server.listen(process.env.PORT) //no final do arquivo
```