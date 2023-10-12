## <span style="color:aquamarine">getElementsByTagName("h1")</span>
- retorna se um elemento do dom existe no documento

![[Pasted image 20231012080006.png|400]]
- Armazena em uma variável e manipula ele dentro do console

![[Pasted image 20231012080203.png|400]]

---
## <span style="color:aquamarine">getElementById</span>
- Selecionar um elemento id

```js
document.getElementById("id da tag");
```

## <span style="color:aquamarine">getElementById</span>
- Seleciona pela classe do elemento('class=')
```js
document.getElementByClassyName("botão");
```

## <span style="color:aquamarine">querySelector</span>
- Seleciona o primeiro elemento
- Retorna o primeiro elemento dentro do documento
```js
document.querySelector("#teste"); //id
document.querySelector(".botao"); //class
document.querySelector("h1"); //tag
```

## <span style="color:aquamarine">querySelectorAll</span>
- Seleciona todos os elementos
- retorna todos os elementos
- Sempre retorna um Array
```js
document.querySelectorAll("li");
```
- selecionar entre camadas (tanto querySelector e querySelectorAll)
```js
querySelectorAll("#teste ul li");
```