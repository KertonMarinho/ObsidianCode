# <span style="color:brown">Eventos do teclado pelo html</span>
## <span style="color:yellow">onkeydown</span>
-  É disparado quando uma tecla é pressionada
- Também se repete quando é segurado
---
## <span style="color:yellow">onkeypress</span>
- É disparado quando uma tecla é segurada
---
## <span style="color:yellow">onkeyup</span>
- É disparado quando uma tecla é solta
- ---
# <span style="color:brown">Eventos do teclado pelo JS</span>
## <span style="color:yellow">addEventListener()</span>
-  Registra uma única espera de evento em um único alvo. O [alvo do evento (en-US)](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget "Currently only available in English (US)") pode ser um único [elemento (en-US)](https://developer.mozilla.org/en-US/docs/Web/API/Element "Currently only available in English (US)") em um documento, o [`documento` (en-US)](https://developer.mozilla.org/en-US/docs/Web/API/Document "Currently only available in English (US)") em si, uma [`janela` (en-US)](https://developer.mozilla.org/en-US/docs/Web/API/Window "Currently only available in English (US)"), ou um [`XMLHttpRequest`](https://developer.mozilla.org/pt-BR/docs/Web/API/XMLHttpRequest).
- Em um elemento:
```js
const input = document.querySelector('input');
input.addEventListener(nome do evento);//pode ser keydown, keypress ou keyup
```
- Em um documento:
```js
document.addEventListener('keyup',nome da funçao); //nome da função = sem aspas e sem parênteses, só o nome dela!
```
### <span style="color:yellow">Função com evento e code(qual tecla foi acionada)</span>
```js
function soltou(e){
	console.log(e.code); //ou event
}
const input =document.querySelector('input');
input.addEventListener('keuup',soltou);
```
![[Pasted image 20231015212555.png|400]]
- Tem também o <span style="color:yellow">key</span>:
- ele e mais simplório, não mostra se aperta tecla shift se é da direita ou esquerda:
```js
function soltou(e){
	console.log(e.key); //ou event
}
const input =document.querySelector('input');
input.addEventListener('keyup',soltou);
```
- ver se determinada tecla foi acionada``e.shiftkey``:
```js
function soltou(e){
	console.log(e.shitkey); //ou event
}
const input =document.querySelector('input');
input.addEventListener('keyup',soltou);
// retorna um bolean
```
