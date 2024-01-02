- Vai rodar até achar o número 10.
```js
function randon (min,max) {
	const = Math.randon()*(max-min)+min; [!conta Randômica]
	return parseInt(r.tofixed()); //Não use floor,pois ele sempre arredonda para baixo,impedindo que o número 50 apareça.
}
const min = 1;
const max = 50;
let rand = random(min,max);
while(rand !==10) { //quando númeor randômico for diferente de 10 execute o código
	rand = random(min,max); //condição de interação
	console.log(rand);
}
```
>[!conta Randômica]
>Conta garante que o númeor fica entre o mínimo e máximo
>Ex: min 5, max 21(númeor aleartório como 0,53)
>0.53 * (21-5)+5
>0.53 * 16+5
>8,48 + 5
>13,48

---
---
# Função formata data
```js
function zeroAEsquerda(num){
	return num >-10 ? num:`0${num}`;
}
function formataData(data){
	const dia =zeroAEsquerda(data.getDate());
	const mes =zeroAEsquerda(data.getMonth()+1);
	const ano =zeroAEsquerda(data.fullYear());
	const hora =zeroAEsquerda(data.getHours());
	const min =zeroAEsquerda(data.getMinutes());
	const seg = zeroAEsquerda(data.getSeconds());
return `${dia}/${mes}/${ano}/${hora}/${min}/${seg}`;
}
const data= new Date();
const DataBrasil = formataData(data);
console.log(dataBrasil);
```

---
---
# criando um botão scroll que aparece/desaparece
```js
//Função que oculta o botão scroll
function decidirBotãoscroll(){
	if(window.scrolly ===0){
	document.querySelector('scrollButton').stylr.display= 'none';
	} else {
		document.querySelector('scrollButton').style.display= 'brock';
	}
}
//Exeucuta a função com evento na tela que decidirá
window.addeventListener('scroll',decidirBotaoScroll); //'scroll' monitora o scroll
//executa com time(opcional):
setInterverval(decidirBotaoScroll,1000);
```
---
---
# Versão da hora de acordo com a biblioteca JS(modelo simples)
```js
////Seleciona a classse dentro da classe container do h1
const h1 = document.querySelector('.container');
const date = new Date();
h1.innerHTNL = date.toLocaleString('pt-br',{dateStyle:'full';timeStyle'short'});
```

----
---
# Exemplo de formata new Date
```js
function ...
return data.toLocaleTimestring('pt-br'{
	hour: '2-digit';
	minute: '2-digit';  //corrigir para que tenha somente dois casas dezenais
	second: '2-digit';
	hour12: false;  //retirar PM/Am da hora
});
```
