1. Cria uma rota para página em ``index.ts
```ts
router.get('/nome', (req: Request, res: Response)=> {
	res.render('pages/nome');
})
``` 
2. cria o mustache na pasta pages
``nome.mustache``
3. Cria um formulário para digitar alguma coisa  e enviar este dados via get
4. Em ``nome.mustache`` digite o cabecalho(header) feito na aula anterior e o footer
```ts
{{>partials/header}}
{{>partials/footer}}
```
5. Escreva o código do formulário(``nome.mustache``):
```html
{{>partials/header}}
<h1> Qual seu nome? </h1>
<form method='get'>
	<input type="text"name="nome" placeholder= "Digite seu nome"/><br>
	<input type= "submit" value= "enviar"/>
</form>
{{>partials/footer}}
```
- Agora fazer uma função para receber esses dados do formulário:
- Tudo que vem depois da interrogação em uma Url se chama ``queryString``
- Para pegar a informação usa-se o ``req(request)``
6. Cria uma string para pegar a query string em ``index.ts
``let nome: string = req.query.nome``
```ts
router.get('/nome', (req: Request, res: Response)=> {
	let nome: string = req.query.nome;=
	res.render('pages/nome');
})
```
7. Declara a variável para que possa ser usada
``res.render('pages/nome',{nome})``

```ts
router.get('/nome', (req: Request, res: Response)=> {
	let nome: string = req.query.nome;=
	res.render('pages/nome',
		nome
	);
})
```
8. Dentro do objeto query string pode vim valores, mas não ten certeza que este item vem uma string para contornar utilize``as string``
- Estamos especificando que o valor desta variável vai ser uma string
```ts
router.get('/nome', (req: Request, res: Response)=> {
	let nome: string = req.query.nome as string;
	res.render('pages/nome',
		nome
	);
})
```
9. Em``nome.mustache`` escreva o código chamando a rota:
```html

{{#nome}}
<hr/>
	opa {{nome}}, tudo bem?
{{/nome}}
{{>partials/footer}}
```