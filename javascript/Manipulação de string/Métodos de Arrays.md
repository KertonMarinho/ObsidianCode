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

