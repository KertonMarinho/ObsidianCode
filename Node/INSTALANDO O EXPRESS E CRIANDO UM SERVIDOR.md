## Criando o servidor
1. Cria o arquivo chamado ``server.ts``, este arquivo ficará rodando em um determinada porta do computador
2. Instale a biblioteca(framework) <span style="color:yellow">Express</span> 

```shell
npm install express
```
3. Para importar, no arquivo``server.ts`` importe a biblioteca
4. Para chamar a função:
````ts
const server = express();
````
5. Para gerar o servidor e escultar a porta
```ts
server.listen(3000);
```
- Geralmente para aplicação Node usamos a porta 3000 (porta padrão para site http 80).
- Para ter autocomplete, como alguma funcionalidades
![[Pasted image 20231004213926.png|400]]

-  instale o type do express
	
```shell
npm install @types/exress
```
6. No ``package.json`` modifique o script ``start-dev`` para:

```json
"start-dev":"nodemom src/server.ts"
```

7. Para acessar o servidor no navegador:

```http
http://localhost:3000
```
- Se aparecer no navegador``cannot get`` significa que está aparecendo, significa que ele não acho a página principal do site, só iniciamos o servidor
8. Criando a página principal
	- Em primeiro lugar tipa o req (request) e o res(response) no import do Express
	```ts
	import express,{request, response} from `express`;
```
	- Criando a rota da página principal
	
```ts
server.get('/'.(req:Request, res: Response)=>{
	res.send('Ola Mundo');
});
```
