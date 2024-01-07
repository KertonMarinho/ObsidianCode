``rotas dinâmicas = leva a várias páginas com o corpo igual``
- parâmetros do get:
```ts
//get(endereço da rota,função)
server.get(rota,(requisiçã0,resposta)=>{})
```
# <span style="color:orange">Rotas estásticas</span>

```ts
server.get('/', (req:Request, res:Response)=>{
res.send('óla Mundo');
});
```

# <span style="color:orange">Rotas dinâmicas</span>

#### <span style="color:yellow">Slug</span>  Titula da notícia que fica lá na url
![[Pasted image 20240106221249.png]]


```ts
server.get('/noticia/:slug', (req: Request, res: Response)=>{
let slug:  string = req.params.slug;
res.send(`notícia: ${slug}`);
});
```


```ts
server.get('/voo/:origem-:destino', (req;Request, res: Response)=>{
	let { origem, destino } = req.params;
	//É a mesma coisa que:
	//let origem = re.parans.origem;
	//let destino = req.params.destino;
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
server.use(mainRoutes); //mesma coisa se fixere assim: server.use('/', mainRoutes);
```
- trabalhando com varias arquivos  de  rotas 
```ts
server.use(mainRoutes); //ou server.use('/', mainRoutes);
server.use('/painel', painelRoutes);
```
