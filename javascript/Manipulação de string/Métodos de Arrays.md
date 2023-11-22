# <span style="color:aquamarine">toString</span> 
- transforma o array um string(separa com virgula)
```js
let lista = ['ovo', 'farinha', 'corante', 'masssa'];
let res = lista.toString();
console.log(res);
//ovo, farinha, corante, massa
```
# <span style="color:salmon">Join</span> 
- Pega o array e transformar em uma string  e separar os itens pelo parâmetro escolhido
```js
let lista = ['ovo', 'farinha', 'corante', 'masssa'];
let res = lista.join('-');
console.log(res);
//ovo-farinha-corante-massa
```

# <span style="color:violet">indexOf</span> 
- Procura um item especifico no array e ele retorna a posição deste item
```js
let lista = ['ovo', 'farinha', 'corante', 'masssa'];
let res = lista.indeOf('corante');
console.log(res);
//2 ( se ele não achar retrona -1)
```
//paou no -06:30