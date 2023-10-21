- É possível trabalhar com duas classes na mesma tag:
```html
<button class="botao azul"></button>
```
---
- lista de classe de um elemento com ``classList``
```js
function clicou(){
	console.log = document.querySelector('button');
	console.log(button.classList);
}
```
---
## Adicionar classes no dom
```js
function clicou(){
	console.log = document.querySelector('button');
	button.classList.add('verde');
}
```
![[Pasted image 20231015102659.png|400]]
---
## Remover classes do Dom
```js
function clicou(){
	console.log = document.querySelector('button');
	button.classList.remove('azul');
}
```
---
### <span style="color:orange">Exemplo de alternar entre classes</span>
```js
function clicou(){
	console.log = document.querySelector('button');
	
	if (button.classList.contains('azul')){
		button.classList.remove('azul');
		button.classList.add('verde');
	}  else {
		button.classList.add('azul');
		button.classList.remove('verde');
	}
};
```
- Um modo de simplificar o código acima é usar o ``toggle``:
#### <span style="color:yellow">toggle</span>
-  remove um token existente da lista e retorna `false`. Se o token não existir, ele será adicionado e a função retornará `true`.
```js
function clicou(){
	console.log = document.querySelector('button');
	button.classList.toggle('azul');
};
```
- ou o ``replace´´
#### <span style="color:yellow">replace</span>
 - troca as classes
 ```js
 function clicou(){
	console.log = document.querySelector('button');
	button.classList.replace('azul','verde'); // assim ele não retorna para o verde
};
//modo de corrgir isso:
function clicou(){
	console.log = document.querySelector('button');
	if(button.classList.contains('azul')){
		button.classList.replace('azul','verde');
	} else {
		button.classList.replace('verde','azul');
	}
```
----

