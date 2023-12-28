# Usando types nos parâmetros de uma função
```js
//...(name: string, lastname: string)
function firstletterUppercase(name: string, lastname: string) {
	let firstLetter = name.charAt(0).toUpperCase();
	return firstLetter+name.substring(1);
}
console.log(firstLetterUppeerCase(kerton));
//Kerton
```
---
# Usando types em retorno de uma função
- como fazer que uma funçõa retorne um type;
- <span style="color:orange">Exemplo 1</span>
```js
//...string): string
function firstletterUppercase(name: string, lastname: string): string {
	let firstLetter = name.charAt(0).toUpperCase();
	return firstLetter+name.substring(1);
}
console.log(firstLetterUppeerCase(kerton));
//Kerton
```
<span style="color:orange">Exemplo 2</span>
```js
function somar(n1: number, n2: number): number {
	return n1 + n2;
}
let alguma = somar(50,30);
```
----
# CONTEXTUAL TYPING EM FUNÇÃO ANÔNIMA

```js
let names = ['bonieky', 'kerton', 'marcio'];
//foreach= dar um loop no array
names.foreach( function(nome)){ //função anônima
  console.log(nome.toUperCase());
				  
}
```
Contextual type: o TS ele verifica o contexto do código ecom base no neste contexto ele vai determinando o type sem que necessariamente vc precise específica essas types:
- Exemplo neste código ele identificou que é um array de strings sem precisar dizer que é um array de strings
- Quando passa o for Each ele sabe que essa função vai só receber dados deste array ele sabe que esse array só tem string
- mas se por um number?
- Como executar o uppercase?
- vc o if ``if(typof nome== 'string'){..usa este código..}
```js
let names = ['bonieky', 'kerton', 'marcio', 90];
//foreach= dar um loop no array
names.foreach( function(nome){ //função anônima
  if (tpyof nome == 'string'){
	  console.log(nome.toUperCase());
	} else {
	console.log(nome);
	}
});
```