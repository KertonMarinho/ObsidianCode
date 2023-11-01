``Promise = promessa
``then = então
![[Pasted image 20231031213617.png|500]]
- Toda função fetch ela retorna uma promessa.

```js
function clicou() {
	fetch(`https://jsonplaceholder.typicode.com/posts`)
		.then((response => { //quando vc tiver resposta execute
			return response.json();
		})
		.the ((json) =>{  //quando vc tiver resposta execute
			alert(`Titulo do primeiro post: ${json[0$.tilte}`)
		});
		)
}
document.querySelector(`#botao`).addEventListener(`click`,clicou());
```
---
# <span style="color:yellow">Catch</span>
- recebe um Callback para ser executado quando der um problema

![[Pasted image 20231031220342.png]]
# <span style="color:yellow">Finally</span>
- Uma função que vai executada mesmo o fetch com erro ou sem erro
```js
function clicou() {
	fetch(`https://jsonplaceholder.typicode.com/posts`)
		.then((response => { //quando vc tiver resposta execute
			return response.json();
		})
		.cath(() =>{
			alert("Deu problema na requisição");
		})
		finally(()=>{
			alert(öPA,ACABOU TUDO!); //fINALLY SEMPRE VAI SER EXECUTADO.
		})
		)
}
document.querySelector(`#botao`).addEventListener(`click`,clicou());
```
