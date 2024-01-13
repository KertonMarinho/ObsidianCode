>[!info]
>Antes de começar o projeto:
>  - Cria um repositório no gitHUb
>  - Clone esse projeto
>  - Abre no vscode

---
### Arquivos de configuração
1. no ``terminal`` do VsCode inicia o ``npm``
```shell
npm init
```
2. Cria o arquivo de configuração do typescript
```shell
tsc --init
```
3. Configure o básico no ``tsconfig.json``
- Em ``Basic options``,coloque essas configurações:
```json
"target": "es6",
```
- outDir e rootDir
```js
"outDir": "./dist",
"rootDir": "./src"
```
- descomente o module resolution em ``Module Resolution Options``
```json
"moduleResolution": "node",
```
---
### Agora instale a dependência que precisa:
1. Instale o Express, Mustache e dotEnv
```shell
npm install express mustache-express dotenv
```
2. Instale as dependências de desenvolvimento (types)
```shell
npm install --save-dev @types/express @types/mustache-express @types/node
```
---
### Pastas do projeto
1. Cria a pasta ``src
2. Dentro da pasta ``src`` cria o arquivo ``server.ts``

---
### Pré-instalação de configuração do PC
- Se não estiver instalado globalmente o Nodemon, Typscript e  Ts-node
```shell
npm install -g nodemon typescript ts-node
```
---
### Configuração do arquivo ``package.json``
1. Em ``package.json`` no objetoJson ``script`` cria o atalho para rodar o projet:
```json
"script": {
...
"start-dev": "nodemon -e ts,json,mustache src/server.ts"
//ts,json,mustache extensões que ele vai monitorar
//src/server.ts arquivo que vai execultar
}
```
---
### Detalhando o Readme

```r
# nodets-canil
Projeto feito no módulo do curso Node + Typescript

### Pré-requisitos globais
`npm i -g typescript ts-node`

### instalação
'npm install'

### Para rodar o projeto
'npm run start-dev'

```
---
### Criando o servidor
1. No arquivo ``server.ts`` importe:
```ts
import express from "express";
import doten from 'dotenv';
import mustache from 'mustache-express';
import path from 'path'; //configuração da pasta pública
```
2. inicia no ``server.ts`` o dotenv
```ts
dotenv.config();
```
3. Cria <u>fora</u> da pasta ``src`` o arquivo ``.env``
4. No arquivo`.env` ,coloque a porta que vai rodar o projeto
```R
PORT=4000
```
5. Inicia o Express no arquivo ``server.ts``
```ts
const server = express();
```
6. Configure o Mustache no arquivo ``server.ts``:
```ts
server.set('view engine', 'mustache');
```
7. Configure as pastas de visualização do projeto
```ts
server.set('views', path.join(__dirname, 'views'));
```
8. cria a pasta ``views`` em ``src``
9. Inicia o mustcache:
```ts
server.engine('mustache', mustache());
```

---
### Criando a pasta pública
1. Cria a pasta `public` fora da pasta ``src``
2. Configure a pasta de arquivos estáticos em `server.ts`
```ts
server.use(express.static(path.join(__dirname, '../public')));
```

3. Dê um espaço em ``server.ts``  para rotas
```ts
//rotas
```
4. Logo depois das rotas, coloque o servidor para rodar na porta especifica
```ts
server.listen(process.env.PORT);
```
5. Cria uma pasta de auxilio do arquivo HTML fora do src, logo no começo `_html`
6. Coloque o arquivo HTML da aula na pasta ``_html``(depois que finalizar o projeto pode deletar essa arquivo)
7. Coloque o arquivo da aula ``css`` e ``images`` na pasta ``public``
---
### Rotas
1. Cria a pasta `` routes``
2. Cria o arquivo`index.ts`na pasta `routes`
3. No arquivo `index.ts` ,importa o ``router``
```ts
import { Router} from 'express';
```
4.  Inicia o ``router``
```ts
const router = Router();
```
5. exportar o ``router``
```ts
export default router;
```
6. Cria a rota ``home``
```ts
router.get('/', (req, res)=> {
	res.send('home');
});
```
7. Na pasta ``server.ts`` importa a rota ``home`` criada:
```ts
import mainRoutes from './routes/index';
```
8. Seta a rota ``home`` em ``server.ts`` no campo reservado das rotas
```ts
server.use(mainRoutes);
```
9. Cria a pasta Não encontrada
```ts
server.use((req, res)=> {
	res.send('página não encontrada!');
});
```
10. No ``terminal`` rode o projeto
```shell
npm run start-dev
```
11. Na pasta ``src``, cria a pasta ``controllers``
12. Na pasta ``src``, cria a pasta ``models``
13. Na pasta ``controllers`` ,cria o arquivo ``pageController.ts``
14. Na pasta ``controllers`` ,cria o arquivo ``searchController.ts``
15. No arquivo `pageController.ts`  importa o Request e Response do express:
```ts
import {Request, Response} from 'express';
```
16. Cria a estrutura na  página `pageController` já exportando:
```ts
export const home = (req:Request, res: Response) => {
	//res.render('pages/page');
};
```
17. Importa o controller <u>Page</u> no arquivo ``index.ts``
```ts
import * as PageController from '../controllers/pageController';
```
18. Importa o controller <u>search</u> no arquivo ``index.ts``
```ts
import * as SearchController from '../controllers/searchController';
```
19. Cria a estrutura na página ``searchController`` já exportando:
```ts
export const search = (req:Request, res: Response) => {
	//res.render('pages/search');
};
```
20. Cria as rotas do <u>controller</u> no ``index.ts``
- Logo depois de ``const router``
```ts
router.get('/'), PageController.home);
router.get('/dogs'), PageController.dogs);
router.get('/cats'), PageController.cats);
router.get('/fishes'), PageController.fishes);
//sinaliza error mais e só cria em pages o proximo passo!
```
21. Em `pageController` cria a estrutura para cada rota:
```ts
export const home = (req:Request, res: Response) => {
	//res.render('pages/page');
};
export const dogs = (req:Request, res: Response) => {
	//res.render('pages/page');
};
export const cats = (req:Request, res: Response) => {
	//res.render('pages/page');
};
export const fishes = (req:Request, res: Response) => {
	//res.render('pages/page');
};

```
22. Cria as rota do <u>search</u> em index.ts
```ts
...
router.get('/fishes'), PageController.fishes);
router.get('/search'), searchController.search);
//sinaliza error mais e só cria em pages o proximo passo!
```
23. Verifique o controller no navegador está funcionando usando ``send``
```ts
//em pageController
export const home = (req:Request, res: Response) => {
	res.sen('home no controller!');
};
```
![[Pasted image 20240110224712.png]]

---
### Separando os `views`
- Pare o projeto `crtl+c``
- Antes começar faça o commit
```shell
git add.
git commit -m "base criada"
git push 
```
- Inicia o projeto `npm run start-dev`

1. Cria em `src`a pasta `views`
2. Na pasta `views`cria  a pasta ``pages`` 
3. Na pasta `views`cria a pasta `partials`
4. Na pasta `partials` cria o arquivo `header.mustache
5. Na pasta `partials` cria o arquivo `footer.mustache`
6. Vá em `html` pegue do começo`` linha 1`` até a `linha 26` (menu: `</nav>)` e recorte para a pasta `header.mustache`
7. Vá em `header.mustache` em ``href= "css/style.css"`` coloque a barra no começo para ele pegar o começo do projeto(`"/css/style.css"`)
8.  Vá em `header.mustache` em ``href= images/favicon.png"`` coloque a barra no começo para ele pegar o começo do projeto(`images/favicon.png"`)
9. No arquivo ``header.mustache`` na class ``container``  coloque barra para ele ser a raiz do projeto(página home)

![[Pasted image 20240111225301.png]]
10. No arquivo `header.mustache` na class `container`, no form  method coloque a barra `/search`em `` action`
![[Pasted image 20240111225740.png|500]]
11. Acrescenta  nos links do projeto:
![[Pasted image 20240111230020.png|500]]

12. Em `html` recorte o rodape
![[Pasted image 20240111230147.png]]
13. Cole em `footer.mustache`
14. Em`viwes`cria a pasta `pages`
15. cria em `pages` o arquivo page.mustache
16. Pego o resto do html e cole em ``page.mustache``
17. No final do arquivo `page.mustache` cole o rodapé
```ts
{{>partials/footer}}
```
18. Em cima do mesmo arquivo, cole:
```ts
{{>partials/header}}
```
19 Para checar se está funcionando no arquivo ``pageController`` escrevas os <u>send</u>:
![[Pasted image 20240112213626.png|500]]
20. Em `pages.mustache`>`class container`>`item` apague todos class item  deixe somente um
![[Pasted image 20240112214116.png|400]]
---
## Deixando a pagina dinâmica, modificando dados em cada página
1. Para enviar dados da página, Em `pagesController`  , const ``home`` cria o objeto e coloque as informações relacioandas a este objeto:
```ts
export const home = (req: Request, res: response) => {
	res.render('pages/page', {
		banner: {
			title: 'Todos os animais',
			background: 'allanimals.jpg'
		}
	});
}
```
2. Coloque uma condicional`{{#banner}}`caso ``banner`` existir aparece o texto "Todos os animais"
```ts
{{#banner}}
<section class="banner" style="backgroun-image: url('images/allanimais.jpg')">Todos os animais</section>
<h2>Todos os animais disponíveis para adoção</h2>
{{/banner}}
```
3. troque o texto `Todos os animais`de `h2` pelo caminho da rota `{{title}}`
```ts
{{#banner}}
<section class="banner" style="backgroun-image: url('images/allanimais.jpg')">Todos os animais</section>
<h2>{{titile}} disponíveis para adoção</h2>
{{/banner}}
```
4. troque a rota da imagem ``allanimais.jpg`` por `{{background}}`
```ts
{{#banner}}
<section class="banner" style="backgroun-image: url('images/{{background}})">Todos os animais</section>
<h2>{{titile}} disponíveis para adoção</h2>
{{/banner}}
```
5. troque o texto em section `Todos os animais` por `{{title}}`
```ts
{{#banner}}
<section class="banner" style="backgroun-image: url('images/{{background}})"> {{ title}}</section>
<h2>{{titile}} disponíveis para adoção</h2>
{{/banner}}
```
6.   Em `pagesController`  , const ``dog``s cria o objeto e coloque as informações relacionadas a este objeto:
```ts
export const dogs = (req: Request, res: response) => {
	res.render('pages/page', {
		banner: {
			title: 'Cachorros',
			background: 'banner_dog.jpg'
		}
	});
}
```
7.   Em `pagesController`  , const ``cats`` cria o objeto e coloque as informações relacionadas a este objeto:
```ts
export const dogs = (req: Request, res: response) => {
	res.render('pages/page', {
		banner: {
			title: 'Gatos',
			background: 'banner_cat.jpg'
		}
	});
}
```
8.   Em `pagesController`  , const ``fishes`` cria o objeto e coloque as informações relacionadas a este objeto:
```ts
export const dogs = (req: Request, res: response) => {
	res.render('pages/page', {
		banner: {
			title: 'Peixes',
			background: 'fishe.jpg'
		}
	});
}
```
9. Checa se as páginas estão funcionando:
![[Pasted image 20240112221017.png|400]]
---
## Ativando o menu
- Uns dois jeitos para ativar o menu seria:
1. Em `pageController` cria um objeto ``menu`` com identificação de qual esta ativo(true) em cada variável
![[Pasted image 20240112222348.png|400]]
- Para página dogs, e vai seguindo colocando true nas páginas ativas:
![[Pasted image 20240112222512.png|400]]
2. No arquivo `header.mustache` coloque uma condicional para cada item ``li``
![[Pasted image 20240112222847.png]] 
- Desconsidera o item acima 1 e 2
- Para deixar o código mais organizado,  criaremos uma função que diz que qual  item esteja ativo e ela retorna um objeto com o item  ativo e o restante como falso. Igual acima mas bem mais organizado.
1. Em `src`cria uma pasta chamado ``helpers`` nesta pasta colocaremos as funções do projeto
2. Cria o arquivo `createMenuObject.ts` dentro da pasta `helpers`
3. No arquivo `createMenuObject.ts` cria o objeto com a função:
```ts
export const createMenuObject = () => {};
```
4. Crie uma string que vai conter o menu que quero que estiver ativo
```ts
export const createMenuObject = (activeMenu) => {};
```
5. Tipa este objeto criado(`activeMenu`)
```ts
type MenuOptions= ' ' | 'all' | 'dog' | 'cat' | 'fisher'
export const createMenuObject = (activeMenu: MenuOptions) => {};
```
6. Paou no -04:27