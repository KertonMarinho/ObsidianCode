- quando usamos o método post podemos enviar dados através do corpo da requisição(dados enviados internamente junto com a requisição), somente o post aceita o corpo da requisição
```js
async function inserirPost() {
	document.getElementById("posts").innerHTML = "carregando...";

	let req = await fetch('https://jsonplaceholder.typicode.com/posts',{
		method: 'post',
		body: json.stringify({
			title: 'Título de teste'
			body: 'corpo do teste'
			userId: 4
		}),
		headers: {
			'content-type': 'application/json'
		}
	});
	let json = await re.json();
	console.log(json);
}
```