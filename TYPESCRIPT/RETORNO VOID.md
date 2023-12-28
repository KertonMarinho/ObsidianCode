- Quando uma função compre seu papel, mas não têm nenhum tipo de retorno,não espera nenhum retorno
```js
function removerElemento(el: HTMLElement): void{
	el.remove();
}
removeElement(document.getElement('teste));
```
- <span style="color:red">obs:</span>   É possível retorna mesmo usando Void quando Tem um type, isso faze que o TP não espere nenhum retorno da função:
```js
type QualqueFuncao = () =>void;

const algo: QualquerFuncao = () => {
	return "blablabla";
}
algo();
```
