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
