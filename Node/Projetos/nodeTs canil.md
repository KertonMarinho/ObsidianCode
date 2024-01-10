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
3. Cria fora da pasta ``src`` o arquivo ``.env``
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


