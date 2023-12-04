# Criando um time que roda em x em x segundos
```js
function showTime() {
	let d =new Date();
	let h = d.getHours();
	let m= d.getMinutes();
	let s = d.getSeconds();
	let txt = h+':'+m+':'+s;

document.querySelector('.demo').innerHTML = txt;
}
let timer = setInterval(showTime, 1000);
```
![[Pasted image 20231202075653.png|400]]
# <span style="color:orange">Exemplo</span>
- SetInterval com controle(botão)
```js
let timer;
function comecar() {
	timer = setInterval(showTime, 1000);
}
function parar(){
	clearInterval(timer);
}
function showTime() {
	let d =new Date();
	let h = d.getHours();
	let m= d.getMinutes();
	let s = d.getSeconds();
	let txt = h+':'+m+':'+s;

document.querySelector('.demo').innerHTML = txt;
}
```

---
# setTimneout
- Roda a função num intervalo de tempo
```js
setTimeout(function() {
	alert("rodou");
}, 2000);
```
<span style="color:orange">Exemplo</span>\
```js
let timer;
function rodar(){
	timer = setTimerout(function(){
		document.querySelector('demo').innerHTML = 'rodou!';
	}, 2000);
}
function parar(){
	clearTimeout(timer);
}
```