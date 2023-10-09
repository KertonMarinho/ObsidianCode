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
- para chamar ``carros[2]();