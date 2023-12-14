- junta arrays
```js
let numeros = [1,2,3,4];
let outros = [...5,6,7,8];
console.log(outros);
//[1,2,3,4,5,6,7,8]
```

<span style="color:orange">Exemplo</span>
```js
let info = {
	nome:'kerton';
	sobrenome:'lacerda',
	idade:99
};
let novaInfo = {
	...info,
	cidade:"Itajai",
	estado: "Santa Catarina",
	país: "Brasil"
};
console.log(novaInfo);
//{nome:"kerton",sobrenome:"marinho", idade: 99,cidade:"Itajai", estado:"Santa Catarina"}
```

<span style="color:orange">Exemplo</span>

```js
function adicionarInfo(info){
	let novaInfo = {
	...info,
	status: 0,
	token:`jkoddoo`,
	data_cadastro: '...'
	};return novaInfo;
}
console.log({nome:'Kerton', sobrenome: 'Lacerda'});
```