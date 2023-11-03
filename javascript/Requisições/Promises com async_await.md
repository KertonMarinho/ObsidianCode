- Usando a async/await faz que o comando fetch espera a requisição
- Só funciona em função
- Para suporta o recurso tem que por ``async`` bem no começo da função
- Ser for Array function:
	``let clicou = async () =>{}
-  substituir o ``then`` e ``catch``.
- ``await = esperar
- pode usar essa fun'vcão em qualquer fetch
```js

async function clicou() {
	let response = await fetch('https://jsonplaceholder.typicode.com/posts')
		let json = await respons.json(); //esperar a resposta,quando devolver ele contínua o código
		alert(`Título do primeiro post: ${json[0].title}`);
		alert("clicou");//executa 'so depois do async'
}
async function inserir(){
	let response = await fetch(
		'https://jsonplaceholder.typicode.com/posts',
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
		});
	let json = await response.json();
	console.log(json);	
}
document.querySelector('#botao').addEventListener('click',clicou());
document.querySelector('#inserir').addEventListener('click',clicou());
```

