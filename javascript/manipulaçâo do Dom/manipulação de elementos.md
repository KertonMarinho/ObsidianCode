### filhos imediatos dos elementos mostrado no console
```js
console.log(teste.children); //teste=id,poder ser também class ou tags
console.log(teste.children[0].children); //para acessar o filho dentro do filho do id
```
---
## <span style="color:red">innerHTML</span> 
- Conteúdo dentro do elemento
- Pode ser usado tanto para consultar como alterar valor
- ele altera todo o conteúdo, deferente do append que adiciona o elemento
```js
document..querySelector('#teste').innerHTML= "<li>item alterado</li>";
```
- acrescentar novo elemento:
```js
document.querySelector('#teste ul').innerHTML += "<li>item alterado</li>";
//ou
document.querySelector('#teste ul').innerHTML= ul.innerHTML + "<li>item alterado</li>";
//tem outras formas mais eficientes
```
## <span style="color:red">innerText</span> 
- Retorna um texto
```js
document..querySelector('#teste ul').innerText= "<strong>item alterado</strong>";
```
![[Pasted image 20231012090939.png|200]]

## <span style="color:red">outHTML</span>
- retorna o elemento de fora
- retorna o próprio elemento e junto com elemento interno
- O filho e o pai
![[Pasted image 20231012091322.png|350]]
---
# Adiciona itens dentro do elemento
## <span style="color:khaki">append</span>
- adiciona o conteúdo que já tem dentro do elemento
- Só funciona para texto
- O método **`append()`** da Interface [`FormData`](https://developer.mozilla.org/pt-BR/docs/Web/API/FormData) adiciona um novo valor dentro de uma chave existente dentro do objeto `FormData` ou adiciona a chave caso ainda não exista.
- [append() Mozilla](https://developer.mozilla.org/pt-BR/docs/Web/API/FormData/append)
-  adiciona no final do conteúdo que já tem
```js
function clicou() {
	const teste = document.querySelector('#teste');
	const url = teste.querySelector('ul');
ul.append('algum item');
}
```
---
## <span style="color:khaki">createElement</span>
- cria o elemento HTML especificado
- [Document.createElement() - (mozilla.org)](https://developer.mozilla.org/pt-BR/docs/Web/API/Document/createElement).
- tem que ser armazenado em uma variável
## <span style="color:khaki">appenchild</span>
- adiciona no final da lista de elementos
- Adiciona um nó ao final da lista de filhos de um nó pai especificado. Se o nó já existir no documento, ele é removido de seu nó pai atual antes de ser adicionado ao novo pai.

```js
function clicou() {
	const teste = document.querySelector('#teste');
	const url = teste.querySelector('ul');
let newLi =document.createElement("li");
newLi.innerTexte = 'item adicionado';
ul.appendChild(newLI);
};
/*
.Algum item
.Algum item 2
.Item adicionado
*/
```
---
## <span style="color:khaki">prepend</span>
- o mesmo que o append
- mas adiciona no começo dom elemento
```js
function clicou() {
	const teste = document.querySelector('#teste');
	const url = teste.querySelector('ul');
let newLi =document.createElement("li");
newLi.innerTexte = 'item adicionado';
ul.prepend(newLI);
};
/*
.Item adicionado
.Algum item
.Algum item 2

*/
```

> [!SUMMARY] Diferenças entre innerHTLM, append e append chlid
> O innerHTML é útil para manipular diretamente o conteúdo do elemento, mexer nele seria equivalente a mexer diretamente no arquivo HTML.
>O append coloca o conteúdo dele ao final do conteúdo atual do elemento (já tem uma diferença bem significativa aqui), fora que ele aceita objetos do DOM, enquanto o innerHTML só aceita strings (o que é bem relevante quando você precisa usar o createElement por exemplo).
>E o appendChild é o mesmo que o append só que ele só aceita objetos do DOM e não strings (o que é algo útil quando você começa a se importar com os tipos da sua aplicação, o que é algo bem importante para não criar bugs inesperados nela).

---
# Adiciona item antes ou depois de um elemento

## <span style="color:yellow">After and before</span>

- significa ``after = depois``e ``before = antes``
-  cria um [pseudo-elemento](https://developer.mozilla.org/pt-BR/docs/Web/CSS/Pseudo-elements) que é o último filho do elemento selecionado
- Adicionando texto
```js
function clicou() {
	const teste = document.querySelector('teste');
	const ul = teste.querySelector('ul');
	ul.after("texto qualquer");
}
```
![[Pasted image 20231012102216.png]]
- Adiciona um elemento 
- Primeiro cria o elemento com ``createElement();
```js
function clicou() {
	const teste = document.querySelector('teste');
	const ul = teste.querySelector('ul');
	
	const newButton = document.createElement('button';
	newButton.innerHTML = "Botão";
	
	ul.after(newButton);
}
```


