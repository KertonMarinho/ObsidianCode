- Model View Controller(modelo de controle de visualização)
- É um conceito que divide o site pelo menos três áreas distintas
- <u>Model</u>: Processa os dados
- <u>View</u>: separar em pasta o código responsável pela visualização
- <u>Controller</u>: Quem faz o gerenciamento de todos(recebe dados, chama os Models e etc)
---
# <span style="color:yellow">CONTROLLERS(gerenciador)</span>
- Ajustando a o código das aulas passadas para o conceito MVC
1.  cria o pasta ``controller`` na pasta ``src``
	- Geralmente cria arquivos controllers para cada grupo de informações(home; páginas institucionais como termos de uso, política de privacidade, página de contato; páginas de produto)
2. Cria na pasta ``controller`` o arquivo``homeController.ts``(pode ser ``home.controller.ts,home.ts)
3. Agora recorte a função  da rota home do arquivo ``index.ts`` para essa página

![[Pasted image 20240105105607.png|400]]
4. Cole dentro da variável `` const home``
![[Pasted image 20240105105907.png|400]]
5. import o request e o response:
![[Pasted image 20240105105943.png|400]]
 6. Export a variável home
![[Pasted image 20240105110100.png]]
6. Agora import a página do homeController para o arquivo``index.ts``

![[Pasted image 20240105110234.png|600x100]]
- pode importar o arquivo inteiro do controle se assim desejar:
```ts
import * as HomeController from '../controllers/homeControlller'
```
7. Na rota Home da página do arquivo ``index.ts`` coloque ``homeController.home``
---
---
## Agora vamos transferir a rota de <u>contato</u> e <u>de sobre</u> para pasta ``controllers``:
1. Cria na pasta``controllers`` o arquivo ``infoController.ts`` 
2. Na página em branco
3. Importa o request e o response
```ts
import {Request, Response} from 'express';
```
4. cria a variável ``const contato
5. Exporta essa variável 
``export const contato= ``
6. Recorta  a rota do contato arquivo ``index.ts``
![[Pasted image 20240105111748.png|400]]
7. Coloque a rota no ``infoController``
```ts
export const contato = (req: Request, res: Response) =>{
	res.render('pages/contato');
};
```
8.  Recorta  a rota do sobre arquivo ``index.ts``
![[Pasted image 20240105112115.png|400]]
9.  Coloque a rota no ``infoController``
```ts
export const sobre = (req: Request, res: Response) =>{
	res.render('pages/sobre');
};
```
10. Agora importa a pasta no arquivo ``index.ts``
```ts
import * as infoController from '../controllers/homeControlller'
```
11. Agora na rota do <u>contato</u> use o caminho:
```ts
router.get('/contato', infoController.contato);
```
12. Na rota do <u>sobre</u> use o caminho:
```ts
router.get('/sobre', infoController.sobre);
```
---
---
# AGORA VAMOS TRANSFERIR AS PARTE RELACIONADAS AO USUÁRIO
1. Cria na pasta ``controllers`` o arquivo ``userController``
2. No arquivo vazio, importa o Request e o Response:
```ts
import {Request, Response} from 'express';
```
3. Exportar e cria a variável ``nome``
```ts
export const nome=
```
4. Recortar no arquivo ``index.ts``  a rota do ``/nome``
![[Pasted image 20240105113353.png|400]]
5. Cole na pagina nome:
![[Pasted image 20240105113429.png|400]]
6. recorta a rota da `/idade`
![[Pasted image 20240105113521.png]]
7. Cole a rota da idade, com tem duas  funções idade mude o nome da variável
![[Pasted image 20240105113754.png]]
8. Recorta  a rota ``/iade-resultado``
![[Pasted image 20240105113904.png|400]]
9. Cole e já cria exportando variável ``export const idadeAction``
![[Pasted image 20240105114031.png]]
10. Importa no arquivo ``index.ts`` o arquivo ``userController``
```ts
import * as UserController from '../controllers/userControlller'
```
11. Utilize na rota e importação da rota:
```ts
router.get('/nome', UserController.nome);
```
12. Coloque na rota para exibir o formulário:
```ts
router.get('/idade', UserController.idadeForm);
```
13. E na rota ``/idade-resultado``
```ts
router.get('/idade-resultado', UserController.idadeAction);
```
14. Não precisa mais do Request e Response no arquivo ``index.ts``, então elimine-os

![[Pasted image 20240105115009.png|400]]



>[!info]
> Agora o arquivo de rotas`` index.ts`` está unicamente para as rotas!

---
---
# <span style="color:yellow">MODELS(Gerenciador)</span>

1. Cria a pasta ``models`` em ``src``
2. Cria na pasta ``models`` o arquivo Product.ts
- "para dar o nome aos models  ,geralmente põe no singular com pascal case relacionado ao tipo que vai trabalhar(ex: produto)"
3. Como ainda não trabalhamos com banco de dados, vamos criar uma variável com produtos de exemplo:
```ts
const data = [
	{title:'produto x', price: '10'},
	{title:'produto y', price: '15'},
	{title:'produto w', price: '20'}
];
```
4. Agora cria a tipagem da variável data
```ts
type Product = {
	title: string,
	price: number
};
cosnt data: Product[]=[
	{title:'produto x', price: '10'},
	{title:'produto y', price: '15'},
	{title:'produto w', price: '20'}
];
```
5. Agora cria a função que pega todos os produtos do banco de dados e exporta o banco de dados, que representa de exemplo de banco de dados a variável data:
```js
export const Product = {
	getAll: ()=> {
		return data:
	}
};
```
6. Agora tipa esta função(``product[]``):
```js
export const Product = {
	getAll: Product[] ()=> {
		return data:
	}
};
```
---
## como filtras os dados do banco de dados fictício com uma função:
```ts
export const Product = {
	getAll: Product[] ()=> {
		return data:
	},
	getFromPriceAfter: (price: number): Product[] => {
		return data.filter(item => {
			if(item.price >= price) {//ele vai filtrar pelo parâmetro que vc puser
				return true;
				} else {
					return false;
				}
			}
		})
	}
};
```
- Pode simplificar a função:
```ts
export const Product = {
	getAll: Product[] ()=> {
		return data:
	},
	getFromPriceAfter: (price: number): Product[] => {
		return data.filter(item => item.price >= price);
	
```
2. Na pasta``home.controller.ts`` 
```ts
import { Product} from '.../modela/Product';
```
3. Cria uma variável para chamar a função criada para filtrar
![[Pasted image 20240105223521.png]]
4. na rota ``pages/home`` remove os produtos, porque não é mais necessário:
![[Pasted image 20240105223631.png|300]]
5. Agora mande a lista para substituir o que vc apagou:
![[Pasted image 20240105223755.png]]
- Models ->Products
- views -> home.mustache
- controller -> homeController

>[!info]
>- Models ->Products
>- views -> home.mustache
> - controller -> homeController

>[!info]
> O mustache é utilizado hoje? ou é mais feita manutenção e atualizações em sistemas que utilizam eles? e aprender ele agora é um conceito bom para dar manutenção, somente? usarei mais react ao em vez do mustache?
>- Sim, ele ainda é utilizado, mas apesar do React ser um Mustache só que melhor, eles atuam em problemas/situações diferentes, então seria como comparar laranjas e maçãs, não tem muito ponto nisso.
>- React é garantia de mais complexidade num sistema, e muitas vezes você não precisa disso, você só precisa de algo simples para passar uns dados do banco de dados para o HTML, e nesses casos usar uma template engine como o Mustache é muito mais simples do que ter que preparar todo o projeto e infraestrutura para suportar uma tecnologia mais completa como o React.
>- Agora se o seu front-end for ter mais dependência de JS para tornar tornar o site mais interativo, então React passa a ser uma opção melhor a se considerar.

