- arranjo, variáveis indexadas, vetor, matriz
- É uma estrututa de dados que armazena uma coleção de elementos de tal forma que cada um dos elementos possa se identificadas por,pelo menos, um índice ou uma chave.
- ``let lista = [1,2,3,4,];
---
### Pega o array com duas matrizes
```js
let lista = ['blabla',['xx',ýy]];
console.log(lista[1][0]);
// xx
```
---
# Operações básicas de array
## <span style="color:yellow">Push</span>
- O método **push()** adiciona um ou mais elementos ao final de um array e retorna o novo comprimento desse array.
```js
let ingredientes = ['agua','farinha'];
ingredientes.push('ovo');
//['agua','farinha','ovo']
```
## <span style="color:yellow">Pop</span>
- O método **`pop()`** remove o **último** elemento de um array e retorna aquele elemento.
```js
let ingredientes = ['agua','farinha'];
ingredientes.pop();
//['agua','farinha']
```
## <span style="color:yellow">shift</span>
- O método **`pop()`** remove o **primeiro** elemento de um array e retorna aquele elemento.
```js
let ingredientes = ['agua','farinha','ovo'];
ingredientes.shift();
//[farinha','ovo']
```
## <span style="color:yellow">Unshift</span>
- O método **`unshift()`** adiciona um ou mais elementos no início de um array e retorna o número de elementos (propriedade `length`) atualizado.
```js
let ingredientes = ['agua','farinha'];
ingredientes.unshift('ovo');
//['ovo','agua','farinha',]
```
---
# Função dentro do Array
```js
let carros['palio', 'monza',function(){...},'uno'];
```
- para chamar a função dentro do Array
```js
carros[2]();
```
---
## <span style="color:yellow">JOIN</span>
- Gera uma string 
- O método **`join`**() junta todos os elementos de um array em uma string e retorna esta string.
- Específica uma string para separar cada elemento adjacente do array. O separador é convertido em uma string se necessário. Se omitido, os elementos do array são separados com uma vírgula (","). Se o for uma string vazia, todos os elementos são juntados sem nenhum caracter entre eles.`separador`
```js
let fruits = ['maça', 'uva', 'laranja', 'banana'];
console.log(',');
//maça,uva,laranja,,banana
console.log('-');
//maça-uva-laranja-banana
//obs: join gera um array, tem que salvar em algun lugar
```
---
### Alterar  o último item será saber quantos itens tem:
```js
let fruits = ['maça', 'uva', 'laranja' ,'banana'];
fruits[fruits.length - 1] = pêra;
console.log(fruits);
//['maça', 'uva', 'laranja', 'banana']
```
---
## <span style="color:yellow">SORT</span>
- Coloca uma array em ordem alfabetica
```js
let fruits = ['maça', 'uva', 'laranja', 'banana'];
fruits.sort();
console.log(fruits);
//['banana', 'laranja', 'maça', 'uva'];
```
---
## <span style="color:yellow">REVERSE</span>
- Inverte o  array
```js
let fruits = ['maça', 'uva', 'laranja', 'banana'];
fruits.reverse();
//['banana', 'laranja', 'uva', 'maça'];
```
---
# Ordenação de array
- Ordenar um array com objetos
```js
let cars = [
	{brand: 'fiat', year: 2022},
	{brand: 'bmw', year: 2018},
	{brand: 'bmw', year: 2018},
]
cars.sort((a,b) => {  //item a (item da vez) e o próximo item
	if(a.year > b.year) {
		return 1;
	} else if (a.year < b.year) {
		return -1;
	} else {
		return 0;
	}
});
console.log(cars);
//{brand: 'bmw', year: 2018},
//{brand: 'bmw', year: 2018},
//{brand: 'fiat', year: 2022},
```
>[!info]
>function comparar(a, b) {
  > if (a é menor que b em algum critério de ordenação) {
   >  return -1;
  > }
  >if (a é maior que b em algum critério de ordenação) {
   > return 1;
  >}
  >// a deve ser igual a b
  >return 0;
>}
[Array.prototype.sort() - JavaScript | MDN (mozilla.org)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/sort#descri%C3%A7%C3%A3o)
- simplificando:

```js
let cars = [
	{brand: 'fiat', year: 2022},
	{brand: 'bmw', year: 2018},
	{brand: 'bmw', year: 2018},
]
cars.sort((a,b) => {  //item a (item da vez) e o próximo item
	return a.year - b.year;
});
console.log(cars);
//{brand: 'bmw', year: 2018},
//{brand: 'bmw', year: 2018},
//{brand: 'fiat', year: 2022},
```
- simplificando mais ainda:
```js
cars.sort((a,b) => a.year - b.year);
```
---
# INTERAÇÃO COM ARRAY
## <span style="color:yellow">FILTER</span>
- O método **`filter()`** cria um novo array com todos os elementos que passaram no teste implementado pela função fornecida.
- Roda a função e ele vai retornar true ou  false, se ele retornar false ele não aproveita esse item do array
```JS
let fruits = ['banana', 'laranja', 'maça', 'pêra'];
let bigFruits = fruits.filter((item) => {
	if(item.length > 4) {
		return true;
	}else {
		return false;
	}
});
console.log(bigFruits);
//['banana','laranja']
```
- simplificando:
```js
let bigFruits = fruits.filter((item) => item.length > 4;
```
- filter pode ter ``filter(value,index,array)
---
## <span style="color:yellow">EVERY</span>
