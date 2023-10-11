### Diferença de Array para objeto
- <span style="color:orange">Array</span> listagem numerada
- <span style="color:orange">Objetos</span> listagem nomeada(itens nomeados{})
- ---
```js
let personagens = {
	nome: 'bonieky',
	idade: 90,
	país: Brasil,
	olhos: ['preto','azul'],
	caracteristica: {
		força: 20,
		magia: 5,
		stamina: 15
	}
}
```
- p
- Para acessar o Array
```js 
console.log(personagens['nome']); //ou
console.log(personagens.nome); //mais usado
```
- Para acessar itens dentro do objeto dentro do objeto
```js
console.log(personagens.caracteristica.magia);
```
- Para acessar o Array dentro do objeto
```js
console.log(personagens.olhos[1]);
```
---
## Alteração de propriedade

```js
let personagens = {
	nome: 'bonieky',
	idade: 90,
	país: Brasil,
	olhos: ['preto','azul'],
	caracteristica: {
		força: 20,
		magia: 5,
		stamina: 15
	}
}
personagens.nome = 'Pedro';
//nome:'Pedro',
pessonagens.olhos.push('verde');
//olhos: ['preto','azul','verde'],
no array
persosonagens.caractristicas[1].força
```
- Acessar em um Array:
```js
let persogem = {
	nome: 'Bonieky',
	idade: 90,
	carros: [
		{modelo: 'Fiat', cor: 'preto'},
		{modelo: 'Ferrari', cor: 'vermelha'}
	]
}
console.log(personagem.carros[1].modelo);
//Ferrari
```
---
## Função dentro do objeto

```js
let peossoa = {
	nome: 'Bonieky',
	idade: 90,
	nomeCompleto: function() {
		return `${this.nome} ${this.sobrenome}`; //this é propeio objeto:pessoa
	}
	//para chamar:
console.log(pessoa.nomeCompleto());
```
>[!warning]
>Função anonima(Arroy function) não tem pai, não tem acesso ao this
>`nome completo: () => {return`${this.nome} ${this.sobrenome}`}``
>// underfined undefined

>[!info.THIS]
>Refere-se ao próprio elemento que está no contexto
>Só existe dentro do objeto
>Atraves do this, conseguimos acessar os itens propriedade, funções, etc...(dentro das funções)

---





