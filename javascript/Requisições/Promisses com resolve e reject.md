``then = quando vc tiver resultado executa isso
```js
function pegarTemperatura (){
	return new Pormisse(function(resolve, reject){
		console.log("Pegando temperatura...");
		setTimeout(function(){
			resolve('40 na sombra');
		}, 2000);
	});
}
let temp = pegarTemperatura();
temp.then(function(resultado) {
	console.log("TEMPERATURA: "+resultado);
});
temp.catch(function(error){
	console.log("Eita, deu errado!")
});
```
>[!info]
>Só um detalhe é que a promise executa independente de você usar o then ou o catch, você usa eles pois eles são os únicos meios de você acessar os valores internos dela, e aplicar computações neles, pois o dado não pode sair de lá dentro.

