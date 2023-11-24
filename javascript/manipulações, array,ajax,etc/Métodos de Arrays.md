# <span style="color:aquamarine">toString</span> 
- transforma o array um string(separa com virgula)
```js
let lista = ['ovo', 'farinha', 'corante', 'masssa'];
let res = lista.toString();
console.log(res);
//ovo, farinha, corante, massa
```
# <span style="color:salmon">Join</span> 
- Pega o array e transformar em uma string  e separar os itens pelo parâmetro escolhido
```js
let lista = ['ovo', 'farinha', 'corante', 'masssa'];
let res = lista.join('-');
console.log(res);
//ovo-farinha-corante-massa
```

# <span style="color:violet">indexOf</span> 
- Procura um item especifico no array e ele retorna a posição deste item
```js
let lista = ['ovo', 'farinha', 'corante', 'masssa'];
let res = lista.indeOf('corante');
console.log(res);
//2 ( se ele não achar retrona -1)
```
# <span style="color: #1E90FF">pop()</span>
- Remove o último item do array
```js
let lista = ['ovo', 'farinha', 'corante', 'masssa'];
let res = lista.pop();

let res = lista
console.log(res);
//['ovo', 'farinha', 'corante']
```

# <span style="color:red">shift()</span> 
- Remove o primeiro item do array
```js
let lista = ['ovo', 'farinha', 'corante', 'masssa'];
let res = lista.shift();

let res = lista
console.log(res);
//['farinha', 'corante', 'masssa'];
```

# <span style="color: #20B2AA">push</span>
- Adicione um novo item ao array
```js
let lista = ['ovo', 'farinha', 'corante', 'masssa'];
let res = lista.push('prato');

let res = lista
console.log(res);
//['ovo', 'farinha', 'corante', 'masssa', 'plato'];
```
- Alterar um item no Array
```js
let lista = ['ovo', 'farinha', 'corante', 'masssa'];
lista[0] = 'ovos'

let res = lista
console.log(res);
//['ovos', 'farinha', 'corante', 'masssa', 'plato'];
```
- Adicionar um item pelo índice
```js
let lista = ['ovo', 'farinha', 'corante', 'masssa'];
lista[4] = 'liquidificador'


let res = lista
console.log(res);
//['ovo', 'farinha', 'corante', 'masssa', 'plato','liquidificador'];
```
- Adiciona um item pelo índice quando não se sabe o último item(não recomendada seu uso)
```js
let lista = ['ovo', 'farinha', 'corante', 'masssa'];
lista[lista.length] = 'liquidificador'


let res = lista
console.log(res);
//['ovo', 'farinha', 'corante', 'masssa', 'plato','liquidificador'];
```

---
# <span style="color: #00FF00">splice</span> 
- Remover um item do array
- Parâmetro: ``splice(indece que vai remover,quantos itens quer remover apartir do primeiro parâmetro);
```js
let lista = ['ovo', 'farinha', 'corante', 'masssa'];
lista.splice(1,2); //se for um só parâmetro(splice(1);) ele remover todos os iten apartir do [1].

let res = lista
console.log(res);
//['ovo','masssa'];
```
- Para remover um item só ``lista.splice(1,1);

# <span style="color:violet">concat</span> 
- concatena dois arrays
```js
let lista = ['ovo', 'farinha', 'corante','massa'];
let lista2 = ['prato', 'liquidificador', 'forno'];

let res = lista.concat(lista2);

console.log(res);
//['prato', 'liquidificador', 'forno', 'prato', 'liquidificador', 'forno'];
```

# <span style="color: #D2691E">sort</span> 
- Ordena um array em ordem alfabética.
```js
let lista = ['ovo', 'farinha', 'corante', 'masssa'];
lista.sort();
let res = lista
console.log(res);
// ['corante', 'farinha', 'massa', 'ovo']
```
# <span style="color:#FF00FF">reverse</span>
- Inverte a ordem do array
```js
let lista = ['ovo', 'farinha', 'corante', 'masssa'];
lista.reverse();
let res = lista
console.log(res);
// ['ovo','massa','farinha','corante' ]
```

# <span style="color:#6495ED">map</span>
- O método **map()** invoca a função `callback` passada por argumento para cada elemento do Array e devolve um <u>novo</u> Array como resultado.
- mapeia o array e executa a função em cada item do array
```js
let lista = [45, 4, 9, 16, 25];
let lista2 = [];

lista2 = lista.map(function(item) {
	return item * 2;
});
*/*
for(let i in lista){
	lista2.push(lista[i] *2);
}*/
let res = lista2;
console.log(res);
//[90, 08, 18, 32, 50]
```

# <span style="color:#DC143C">filter</span>
- O método **`filter()`** cria um novo array com todos os elementos que passaram no teste implementado pela função fornecida.
- filtra o array e retorna false ou true
```js
let lista = [45, 4, 9, 16, 25];
let lista2 = [];

lista2 = lista.filter(function(item) {
	if(item > 20) {
		return true;
		} else {
			return false
			}
	}
});

let res = lista2;
console.log(res);
```

# <span style="color:#FF4500">every</span>
- O método `every()` testa se todos os elementos do array passam pelo teste implementado pela função fornecida. Este método retorna um valor booleano.
```js
let lista = [45, 4, 9, 16, 25];
let lista2 = [];

lista2 = lista.every(function(item) {
	if(item > 20) {
		return true;
		} else {
			return false
			}
	}
});

let res = lista2;
console.log(res);
//false
```

# <span style="color:#BDB76B">some</span>
- O método **`some()`** testa se ao menos um dos elementos no array passa no teste implementado pela função atribuída e retorna um valor **`true`** ou **`false`**.
```js
let lista = [45, 4, 9, 16, 25];
let lista2 = [];

lista2 = lista.some(function(item) {
	return (item >3)? true : false;
});

let res = lista2;
console.log(res);
//false
```

# <span style="color:green">find</span> 
- O método **`find()`** retorna o <u>valor do primeiro elemento</u> do array que satisfizer a função de teste provida. Caso contrario, [`undefined`](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/undefined) é retornado.
- ``find(function(item,index,array){};)
```js
let lista = [45, 4, 9, 16, 25];
let lista2 = [];

lista2 = lista.find(function(item) {
	return (item == 16)? true : false;
});

let res = lista2;
console.log(res);
//16
```
<span style="color:orange">Exemplo 2</span>
```js
let lista = [
	{id:1, nome:'kerton', sobrenome:'Marinho'}
	{id:2, nome:'Daniela', sobrenome:'Marinho'}
	{id:3, nome:'kevin', sobrenome:'Marinho'}
];
let pessoa = lista.find(function(item){
	return (item.id == 3) ? true : false;
});
let res = pessoa;
console.log(res);
```
# <span style="color:salmon">findIndex</span>
- O método **`findIndex()`** retorna o **índice** no array do primeiro elemento que satisfizer a função de teste provida. Caso contrário, retorna -1, indicando que nenhum elemento passou no teste.
```js
let lista = [45, 4, 9, 16, 25];
let lista2 = [];

lista2 = lista.findIndex(function(item) {
	return (item == 16)? true : false;
});

let res = lista2;
console.log(res);
//3
```