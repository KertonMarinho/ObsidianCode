## <span style="color:purple">onclick</span> 
- O evento executa uma determinada funcionalidade quando um botão é clicado
- forma um de escultar o evento
```html
<button class="botao" onclick="clicou">Clique em min</button>
```
## <span style="color:green">addEventListener</span> 
- registra uma única espera de evento em um único alvo
- escutador de eventos
- forma dois de escultar o evento
```js 
addEventListener("tipode evento", Função que vai execultar);
```
<span style="color:orange">Exemplo</span>
```js
function clicou() {
	console.log("Clicou no botão";
}
let botão = document. querySelector('.botao');
botao.addEventListener("click", () => {
clicou();
})
```