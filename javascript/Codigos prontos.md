# <span style="color:yellow">Função que formata data</span>
```js
function zeroAEsquerda(num) {
	return num >= 10 ? num: `0$num}`;
}
function formataData(data) {
	const dia =zeroAEsquerda(data.getDate());
	const mes =zeroAEsquerda(data.getMonth()+1);
	const ano =zeroAEsquerda(data.getfullYear());
	const hora =zeroAEsquerda(data.gethours());
	const min =zeroAEsquerda(data.getMinutes());
	const seg =zeroAEsquerda(data.getSeconds());
	return `${dia`}/${mes}/${ano}/${hora}/${min}/${seg}`;
}
const data = new Date();
const dateBrasil = formataData(data);
console.log(dataBrasil)
```
---
---

