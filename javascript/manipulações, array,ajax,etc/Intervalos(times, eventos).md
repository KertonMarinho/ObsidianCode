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
