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
