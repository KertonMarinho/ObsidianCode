- Como exibir uma lista:
1. HTML
![[Pasted image 20240103213131.png|260]]
2. Em ``router.get "/"`` -> render -> cria o array Procuts que será a lista de objetos:
```ts
res.render('home'{
		   name:'Kerton',
		   lastName: 'Marinho'',
		   procuts: [
			   {title: 'produto x', price: 10},
			   {title: 'produto y', price: 15},
			   {title: 'produto w', rpice: 20}

		   ]


});
```
- Para exibir no Mustache:
```html
<h2>Produtos</h2>
<ul>
	{{#products}}
		<li>{{title}} - {{price}}</li>
	{{/products}}
</ul>
```

---
- Para usar uma lista simples:
```ts
res.render('home',{
	...
	lista: [
		'Alguma coisa muito legal',
		'Outra coisa'
	]
})
```
- Para exibir no Mustache:
```html
<h2>produto</h2>
...
<ul>
	{{#frasesDoDia}}
		<li>{{.}}</li> //use ponto para listas simples, ele usa aquele loop especifico no momento
	{{/frasesDoDia}}
```