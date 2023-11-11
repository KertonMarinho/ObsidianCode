- Lê imagem e exibir na tela
- pega a própria imagem antes de fazer upload
- Pega essa imagem e já mostra a na tela

1. passo: o input no html:
![[Pasted image 20231110233211.png|500]]
2. no js
- seleciona o objeto file
![[Pasted image 20231110233343.png|500]]
```js
function mostrar() {
	let imagem = document.getElementById(ïmagem).file[0];
}
```
3. com objeto ``file`` gerar apartir dele uma url:
```js
function mostrar() {
	let imagem = document.getElementById(ïmagem).file[0];
	let img = docement.createElement('img');
	img.src = url.createObjectURL(imagem);
	document.getElementById("area").innerHTML = img;
	img.width = 200px;
}
```
---
# Thumbnails com fileReader(leitor de arquivo)

```js
function mostrar(){
	let reader = new fileReader();
	let imagem = document.getElementById('imagem').file[0];
	//precisa fazer uma callback
	reader.onloadend = function(){
		let img = document.createElement(ímg);
		img.src -= reader.result;
		img.width = 200;
		document.getElementById('area').appendchild(img);
	}
	readerAsDataURL(imagem); //lê a imagem
}
```

