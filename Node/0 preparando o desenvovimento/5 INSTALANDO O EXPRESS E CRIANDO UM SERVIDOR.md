## Criando o servidor
1. Cria o arquivo chamado ``server.ts`` na pasta ``src``, este arquivo ficará rodando em um determinada porta do computador
2. Instale a biblioteca(framework) <span style="color:yellow">Express</span> 

```shell
npm install express
```
3. Para importar, no arquivo``server.ts`` importe a biblioteca
```ts
import express from 'express';
```
1. Para chamar a função:
````ts
const server = express();
````
5. Para gerar o servidor e escultar a porta
```ts
server.listen(3000);
//no final da página
```
- Geralmente para aplicação Node usamos a porta 3000 (porta padrão para site http 80).
- Agora tem opções de  autocomplete, como alguma funcionalidades
![[Pasted image 20231004213926.png|400]]

6.   instale o type do express
	- O node não sabe como funciona o Express e dar error na importação
	- com  a isntalaçãp do type do Express some o erro que da na importação do express)
	
```shell
npm install @types/express
```
6. No ``package.json`` modifique o script ``start-dev`` com o nome ``index``para ``server``:

```json
"start-dev":"nodemom src/server.ts"
```
7. Agora inicia o nodemon:
```shell
npm run start-dev
```

8. Para acessar o servidor no navegador:

```http
http://localhost:3000 
<!..quando a porta for diferente da 80 precisa especificar a porta com dois pontos..>
```
- Se aparecer no navegador``cannot get``  significa que ele não acho a página principal do site, mas demonstra que iniciamos o servidor
9.  Mudamos da porta 3000 para a porta 80 no arquivo ``server.ts``
- obs: Listen é o ultimo comando do código
	
```ts
server.listen(80);
```

10. Criando a página principal
	- Em primeiro lugar tipa o req ``{request}`` e o res``{response}`` no import do Express
	```ts
	import express, {Request, Response} from 'express';
```
	- Criando a rota da página principal

```ts
server.get('/',(req:Request, res: Response)=>{
	res.send('Ola Mundo');
});
```
