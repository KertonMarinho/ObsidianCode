## <span style="color:red">Fetch</span>
- A [API Fetch](https://developer.mozilla.org/pt-BR/docs/Web/API/Fetch_API) fornece uma interface JavaScript para acessar e manipular partes do pipeline HTTP, tais como os pedidos e respostas. Ela também fornece o método global [`fetch()` (en-US)](https://developer.mozilla.org/en-US/docs/Web/API/fetch "Currently only available in English (US)") que fornece uma maneira fácil e lógica para buscar recursos de forma assíncrona através da rede
- A função **fetch** ou **Fetch API**, é uma API de busca do Javascript que permite realizar requisições HTTP assíncronas entre uma aplicação web e recursos externos.
- Estrutura do fetch:
```js
fetch (url)
.then (response => {sua Resposta esperada}) //quando receber as resposta execute uma função específica
.catch (error => {Erro se resposta inesperada})
```
``then- significa então
<span style="color:orange">Exemplo de requisição</span>
```js
function clicou(){
	fetch('[jsonplaceholder.typicode.com/posts](https://jsonplaceholder.typicode.com/posts)')
	.then((response) => {
		return response.json //ele(.json) vai converter a resposta  para um objeto
	})
	.the((json)) => { // por exemplo, pegar o titulo do primeiro post,... ...console.log(json[0].title);
		console.log(json);
	}
}
document.querySelector('#botao').addEventListener('clicou', clicou());
```
---
# Como ver uma requisição acontecendo

- Abre o console>network>fetch/XHR (ele mostra as requisições que acontecerão):
![[Pasted image 20231029223144.png|500]]

- clicando em post ele mostra a resposta, cabeçalho, etc:
![[Pasted image 20231029223343.png|500]]
- Menus do fetch:
![[Pasted image 20231029223843.png]]
``headers = cabeçalho
``payload = 0 que ele mandou de dados nesta requisição
``preview = previa da resposta
``timing = o tempo que durou a requisição

