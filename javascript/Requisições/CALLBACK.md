``CALL BACK = LIGAR DE VOLTA
- Criando uma função, que será passada para uma parte do código(uma outra função por exemplo) que decidirá quando será executada.
- Função que vai lidar com resultado no futuro.
``função Callback:
```js
function clickCallback(){
	alert('clicou no botão');
}
document.querySelector('#botão')
	.addEventListener('click', clickCallback);
//evento listener que vai decidir quando vai aparecer o alert
```
<span style="color:orange">Exemplo 2:</span>
```js
function alertar() {
	console.log("Opa,tudo bem?");
}
let mo,e = 'kerton';
setTimeout(alertar, 2000);
let sobrenome = 'Marinho';
console.log("Nome completo = "+nome+;' '+sobrenome);
```
![[Pasted image 20231107214005.png|300]]
