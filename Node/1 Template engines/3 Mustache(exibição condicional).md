<span style="color:orange">Exemplo</span>
- Mensagem condicional

1. Adicione um novo item no render``(index.ts->router.get/)`` 
```ts
router.get('/',(req: Request, res: REsponse)=>{
	res.render('home', {
		name:kerton,
		lastName: Marinho,
		showWelcome: false //novo item,não aparecer(false),acesso a esta variável dentro do mustache
	});
});
```
- Dentro do ``home.mustache``
- Tem que abrir e fecha a variável``{{#showWelcome}}...{{/showWelcome}}``
![[Pasted image 20240103212447.png|360]]
