# <span style="color:yellow">FOR</span>
```js
for(variável auxiliar,condição, inclemento){}; //for(começa condição,quantas vezes, inclemento){};
for(let i; i<50; i++){};
```
<span style="color:orange">Exemplo</span>
```js
let cores = ['preto', 'branco','azul','vermelho'];

for (let n = 0; n < cores.length; n++) {
	console.log(cores[n]);
}
```
---
### LOOP I IN
```js
for(let i in cores){
	CONSOLE.LOG(CORES[I]);
}
//I = RODA NÚMERO DE VEZES PELO NÚMERO DE ELEMENTOS DE UM ARRAY
//IN = VERIFICA SE UMA PROPRIEDADE EXISTE EM UM OBJETO
```
---
### LOOP FOR OF
```JS
for (let cor of cores){
	console.log(cor);
}
```
---
- Acessar Array com objetos:
```js
let cores = [
	{nome: 'preto', qt: 10},
	{nome: 'azul', qt: 5},
	{nome: 'vermelho', qt: 15}
]
for(let cor of cores){
	console.log(cor.name);
};
for(let i in cores){
	CONSOLE.LOG(CORES[I].name);
};
for (let n = 0; n < cores.length; n++) {
	console.log(cores[n].name);
```
---
# <span style="color:yellow">loop while(enquanto)</span>
- Enquanto a condição for satisfatória ele vai executar o código.
- Quando não sabemos quantas repetições deverá ocorrer.
```js
while (condição){
	arg1; //parâmetro
	c++; //inclemento
}
```
<span style="color:orange">Exemplo</span>
```js
let numero = 0;
while (numero < 10){
	console.log(`O número da vez é ${numero}`);
	numero++; //evita loop infinito
}
```

### Usando while em uma sequência randômica, com parâmetros de parada com o número 10 :
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

>[!warning]
>while = checa a condição, executa o código
>Do While = excuta o código, depois checa a condição
>Se a codição for false logo no começo o Do While para a execução
>Do {
>rand = random(min.max);
>	console.log(rand);
>} whilke (rand !== 10);

