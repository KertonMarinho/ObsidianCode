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
