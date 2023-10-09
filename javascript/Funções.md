- Conjunto de instruções que execulta uma tarefa ou calcula um valor.
- ``entrada ->processamento -> saída``
```js
function nome da funçao (argumentos){ código da função} 
```
- quando o nome da função for uma palavra, letra minuscula
- quando for mais de uma palavra utilize Camel case`nomeSobrenome`
- para usa a função:
```js
nomeDaFunção();
```
---
# Arrow Functions
- função normal
```js
function somar(x+y) {
return x + y;
}
```
- função abreviada
```js
const somar=(x+y) =>{
return x+y;
}
//quando tem uma função que tem maisn de duas linhas obrigatóriamente tem que abrir as chaves
```
- Arrow function
```js
const somar = (x+y) => x+y;
```
- quando tem um parâmetros pode remover parênteses
```js
let letrasNoNome = nome => nome.length;
```
---
## Função dentro de função
- Geralmente para organizar melhor o código
```js
function addSquares(a,b) {
	function square(x){
		return x * x;
		}
	let sqrA = square(a);
	let sqrB = square(b);
	return sqrA + sqrB;
}
COnsole.log(addSquare(2,3));
```
- para deixar mais organizado o código utilize Arrow function dentro da função
```js
function addSquares(a,b) {
	const square = (x) => return x * x;
	
	let sqrA = square(a);
	let sqrB = square(b);
	return sqrA + sqrB;
}
COnsole.log(addSquare(2,3));
```
---
