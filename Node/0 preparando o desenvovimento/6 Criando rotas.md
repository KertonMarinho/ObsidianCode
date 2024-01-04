``rotas dinâmicas = leva a váeias páginas com o corpo igual``
- paramêtros do get:
```ts
server.get(rota,(requisiçã0,resposta)=>{})
```
# <span style="color:orange">Rotas estásticas</span>

```ts
server.get('/', (req:request, res:response)=>{
res.send('óla Mundo);
});
```

# <span style="color:orange">Rotas dinâmicas</span>


```ts
server.get('/noticia/:slug', (req: Request, res: Response)=>{
let slug:  string = req.params.slug;
res.send(`notícia: ${slug}`);
});
```


```ts
server.get('/voo/:origem-:destino', (req;Request, res: Response)=>{
	let { origem, destino } = req.params;
	res.send('procurando voos de ${origem} até ${destino}');
});
```
---
# Separando as rotas no seu lugar
1. Cria a pasta no trabalho ``routers``
2. novo arquivo nas rotas ``index.ts``
3. Importa neste arquivo a biblioteca do Express ``Router``

```ts
import {Router} from 'express';
```
4. Cria uma variável para receber a função ``Router();``
```ts
const router = Router();
```
5. acrescenta a tipagem no import
```ts
import{Router,Request, Response} from 'express';
```
6. cria as rotas, lembrando que tem que por os types``Request e Response``
```ts
router.get('/',(req: Request, res:Response)=>{
	res.send('Óla Mundo');
});
router.get('/contato',(req: Request, res:Response)=>{
	res.send('formulário de contato');
});
```
7.Agora exporta o arquivo:
```ts
export default router;
```
## Agora no arquivo do servidor ``server.ts`` import as rotas
```ts
import mainRoutes from `./routes/index';
```
8. Insira elas no servidor
```ts
server.use(mainRoutes);
```
- trabalhando com varias arquivos  de  rotas 
```ts
server.use(mainRoutes); //ou server.use('/', mainRoutes);
server.use('/painel', painelRoutes);
```
