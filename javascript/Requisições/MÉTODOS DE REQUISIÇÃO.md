### Cabeçalho de requisição no console do navegador
-  Ver qual requisição foi enviado
`` console>Network>post>Heardes>general?request method
>[!warning]
>Quando não manda nada no Fetch o padrão é o método GET

---
## Métodos de requisição

> [!note] Métodos
> get=pegar(pegar informações)
>post=postar/enviar(inserir uma informação)
>put=botar(alterrar uma informação que já existe)
>Deelete

<span style="color:orange">Exemplo</span>
```js

function clicou() {
	fetch('https://jsonplaceholder.typicode.com/posts')
		.then((response => { //quando vc tiver resposta execute
			return response.json();
		})
		.the ((json) =>{  //quando vc tiver resposta execute
			alert(`Titulo do primeiro post: ${json[0$.tilte}`)
		})
}
function inserir(){
	fetch(
		'https://jsonplaceholder.typicode.com/posts'
		{
			method: 'post',
			headers: {
				'content-type': 'aplication/json' //forma que vai mandar o body
				},
				body: json.stringify({ //função que tradz o objeto em um json
					tiltle : 'título de teste', //objeto/post
					body: 'corpo de terste',
					userID: 2
					
				})
		}
	})
	//função que vai teazer  a resposta se deu tudo certo
	.then((response) => { //pega a resposta e converta em objeto
		return response.json();
	})
	.then((json) =>{
		console.log(json);
	}
}
document.querySelector('#botao').addEventListener('click',clicou());
document.querySelector('#inserir').addEventListener('click',clicou());

```

![[Pasted image 20231102090822.png|300]]![[Pasted image 20231102090905.png|400]]




