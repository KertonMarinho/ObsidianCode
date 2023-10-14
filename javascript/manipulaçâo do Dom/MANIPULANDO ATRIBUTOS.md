- Atributos(propriedades dos elementos)
## <span style="color:yellow">getAttribute</span>
- método da [`Element`](https://developer.mozilla.org/en-US/docs/Web/API/Element)interface retorna o valor de um atributo especificado no elemento.
```js
console.log(input.getAttribute('type'));
```
---
## <span style="color:yellow">hasAttribute</span>
- Pesquise se há atributo especificado 
- Volta um bolean
```js
if(input.hasAttribute('placeholder')){
	console.log('Tem placeholder');
} else {
	console.log("Não tem placeholder");
	};
```
---
## <span style="color:yellow">setAttribute</span>
- Define o valor de um atributo no elemento especificado. Se o atributo já existir, o valor será atualizado; caso contrário, um novo atributo será adicionado com o nome e valor especificados.
```js
setAtribute('name','value');
```
<span style="color:orange">Exemplo</span>
```js
function(clicou){
	const input = document.querySelector('input');
	if (input.getAttribute('type') === 'text') {
		input.setAttribue('type', 'password');
	}else {
		input.setAttribute('type','text');
	}
}
```