- existe três formas de fazer uma função

# <span style="color:orange">1° forma </span>
```js
function somar(x, y) {
	return x + Y;
}
```
# <span style="color:orange">2° forma </span>
```js
let somar= function (x, y) {
	return x+y;
}
```

# <span style="color:orange">3° forma(Arrow Function) </span>
```js
let somar = (x, y) => {
	return x +y;
}
```
- expressão direta:
```js
let somar =(x, Y) => x = y;
```
- Quando tem um só parâmetro:
```js
let letrasNoNOme =(nome) {
	return nome.length;
}
//reduzindo:
let letrasNoNOme = (nome) => nome.length;
//Parênteses é opcional quando têm um só parâmentro:
let letrasNoNome = nome => nome.length;
//tendo duas ações deve ser usado os colchetes
```
