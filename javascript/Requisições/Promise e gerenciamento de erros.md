# <span style="color:salmon">Promise</span> 
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
		.them ((json) =>{  //quando vc tiver resposta execute
			alert(`Titulo do primeiro post: ${json[0$.tilte}`)
		});
		)
}
document.querySelector(`#botao`).addEventListener(`click`,clicou());
```
---
##  <span style="color:yellow">Catch</span>
- recebe um Callback para ser executado quando der um problema

![[Pasted image 20231031220342.png]]
## <span style="color:yellow">Finally</span>
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
---
# <span style="color: #1E90FF">Códigos de status de respostas HTTP</span>
- Os códigos de status das respostas HTTP indicam se uma requisição HTTP foi corretamente concluída. As respostas são agrupadas em cinco classes:
1. Respostas de informação``(100-199)
2. Respostas de sucesso``(200-299)
3. Redirecionamento ``(300-399)
4. Erros do cliente ``(400-499)
5. Erros do servidor``(500-599).

<span style="color:orange">Exemplo</span>
<span style="color:green">200 ok</span>
- Estas requisição foi bem sucedida. O siginificado do sucesso varia de acordo com o método HTTP.
<span style="color: #00FF00">201 Created</span>
- A requisição foi bem sucedida e um novo recurso foi criado como resultado. Este é uma tipica resposta enviada após uma requisição POST.
``pouco usado!

<span style="color:red">301 Moved Permently</span>
- Esse código de resposta significa que a URL do recurso requerido mudou. Provavelmente, a nova URL será especificada na resposta.
https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Status
