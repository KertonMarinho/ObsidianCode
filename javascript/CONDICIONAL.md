                                 # Condicional independente
```js
if( );
if( );
if( );
```
# Condicional dependente
```js
if(){}
else if(){
else if(){}
```
----
# condicional ``==`` ou ``===``
### ``==``
- verificação não restrita
- aceita valores parecidos como ``number`` e ``string``
### ``===``
- verificação restrita
- não aceita valores parecidos

```js
let w ="10";
let z = 10;
console.log(w==z);  //true
console.log(w===z); //false
```
---
## Multi-condicional (&& e ||)
- Duas condição precisa ser satisfeita para que funcione para código``(AND = &&)``
```js
if(hora >=12 && hora <18){};
```
- Somente uma das duas precisa ser satisfeita``(or = ||)``
```js
if(hora ==12 || hora == 18){};
```
---
# Condicional dupla
```js
let idade =18;
if(idade < 18){
	console.log("Você é uma criança");
} else if (idade >= 18 && idade < 60){
	console.log("Você é um adulto");
} else if (idade > 60){
	 console.log ("Você é um idoso")
}
```
- casa a primeira condição não seja satisfeita pula para segunda
- caso a segunda condição não seja satisfeita pula para terceira
- ---
## Pode jogar uma condicional dentro do if
```js
let idade = 14;
let verificação = idade >18;
if (verificação){
	console.log("Entrou no IF");
} else {
	console.log("Não entrou no IF")
}
}
//lembrando que só pode ter um else, senão tem quer usar (else if)
```
## Condicional tenário
```js
let adult = (condição)? true : false;
//(condição)?'valor verdadeiro': 'valor falso';
```
- vc pode por entre parênteses
```js
let adult = (age >= 18)? sim : não; //or
let adult = ((age >= 18)? true: false);
```
---
# <span style="color:yellow">Switch</span>
- Condicional com múltiplos resultados
```js
let profession = "fiscal";

switch (profession) {
	case 'Fiscal':
		console.log('Sua camisa será verde');
		break;
	case 'Bombeiro':
		console.log('Sua camisa será vermelha');
		break;
	case 'policial':
		console.log('Sua camisa será azul');
		break;
	default : //nenhum das condiçoes acima forem satisifeitas
		console.log('Sua camisa será padrão');
//defailt = siginifica padrão	
}
```
>[!Operadores de comparação]
> diferente != (não muito usado)
> diferente estrito !==
> 
>

---
# Avaliação curto-circuito(short-circuit)
 - Na operação lógica &&, apartir do momento que tiver false ela vai retorna o valor false (avaliação curto-circuito)
		``&& -> false && true -> false``
```js
console.log('Kerton'&& 0 && 'Maria');
//0
//se fosse todos os valores verdadeira , ele vai retornar a ultima verdadeira
console.log('Kerton'&& true && 'Maria');
//Maria
```

>[!Operadores de comparação]
> Operador False
> false
> 0
> Simbolos com vazio ``ou " " ou ' '
> null / underfined
> NaN = not a number

- Pegadinha curto circutio
```js
const a = 0;
const b = null;
const c = 'false'; //essa é verdadeira, pois uma string é avaliado em verdadeiro
const d = false;
const e = Nan;
console.log(a || b || C || d || E);
//false (string)
// A operação || (or) vai retorna a primeira que for verdadeiro
```




