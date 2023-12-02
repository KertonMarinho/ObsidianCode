# <span style="color:#20B2AA">round</span>
-  Arredondar o número dependendo do próprio número(round)
```js
let novoValor  = Math.round(3.67);
coosole.log( nvo Valor);
//4
```
----
# <span style="color: #1E90FF">floor</span>
- Arredondar para baixo.
```js
let novoValor  = Math.floor(3.67);
coosole.log( nvo Valor);
//3
```
- sempre arredonda para baixo, mesmo que seja 3,99
----
# <span style="color: #00FF00">ceil</span> 
- Arredondar para cima.
```js
let novoValor  = Math.ceil(3.67);
coosole.log( nvo Valor);
//4
```

- Mesmo que seja 3.01 sempre vai arredondar para cima
 ----
# <span style="color:violet">abs</span> 
-  Calcular o valor absoluto de um número.
```js
let novoValor  = Math.abs(-9.65464);
coosole.log( nvo Valor);
//9.65464
```
---
# <span style="color:red">min</span> 
- Retornar Menor número especificado

```js
let novoValor  = Math.min(7,100, 600, 20, 3);
coosole.log( nvo Valor);
//3
```
---
# <span style="color:aquamarine">max</span> 
- Retornar o maior número especificado
```js
let novoValor  = Math.max(7, 100, 600, 20, 3);
coosole.log( nvo Valor);
//600
```
---
# <span style="color:#8B4513">Random</span> 
-  Retornar um número aleatório entre 0 e 1

```js
let novoValor  = Math.round();
coosole.log( novo Valor);
//0.18284783929
```
#### Para retornar um número de 0 a 50, combina funções:
- multiplique pelo número máximo determinado e depois arredonda para baixo com a função floor
```js
let novoValor  = Math.floor(Math.round()* 100);;
coosole.log( novo Valor);
//88
//97

```
- neste caso somente vai até 99.