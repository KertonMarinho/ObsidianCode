1. No arquivo``server.ts
2. 
```js
//sempre depois das rotas:
//server.use(mainRoutes);
server.use((req: Request, res: Response) =>{
	res.status(404).send('Página não encontrada!');
});
```
