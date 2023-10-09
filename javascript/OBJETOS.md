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