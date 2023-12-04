Objeto:
```js
leet pessoa = {
	nome: 'Kerton',
	sobrenome: 'Marinho',
	idade: 120,
	social: {
		facebook: '@kerton',
		instagram: '@kerton'
	},
	nomeCompleto: function() {
		return `${this.nome} ${this.sobrenome}`;
	}
};
cosonloe.log (pessao.social.facebook);
```
## Descontruindo um objeto
- é pegar uma informação especifica de um objeto e transformarem uma variável
- Descontruindo objeto vc colocar em chaves os objetos que vc quer descontruir colocando em uma variável igual ao exemplo abaixo:

```js
let{ nome, sobrenome, idade} = pessoa;
console.log(nome, sobrenome, idade);
//kerton marinho 120
```

- Vc pode mudar o nome da variável que vai ser descontruída:
```js
let {nome:pessoaNome, sobrenome, idade} = pessoa;
console.log(pessoaNome, sobrenome, idade);
//Kerton Marinho 120
```
- Pode por valor padrão para variável, mesma não esteja definida:
```js
let {nome:pessoaNome, sobrenome, sexo = masculino} = pessoa;
console.log(pessoaNome, sobrenome, idade);
//Kerton Marinho 120
```
- Pega objetos dentro dos objetos(primeira forma):
```js
	let { facebook, instagram} = pessoa.social;
```
- Pega objetos dentro dos objetos com outras vaiáveis:
```js
	let { nome, idade, social:{ instagram}} = pessoa;
	console.log(nome, idade, instagram);
	//kerton 120 @kerton
```