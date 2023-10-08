
---
## TYPEOF
- Tipo de dados:
	- number
	- string
	- bolean
```js
typeof idade;
|> number
```
---
# LET,VAR E CONST
<span style="color:orange">LET</span>
- Funciona apenas no contexto que ela foi criada
- Somente no escopo específico do código
- ela poder ser chamada apenas naquela função
- escopo local
<span style="color:brown">VAR</span>
- escopo global
- Ho isting - enviada para escopo geral da tela
<span style="color:purple">const</span>
- escopo valor constante(algo que não muda)
- não modificável
- mais usados no Array ou Objeto
- ----
## concaterna uma string
- concaternar
	```js
	var nome da variável = nome = sobrenome;
	|> nomesobrenome
```
## Colocar espaço sobre as strings
```js
var nome da variável = nome+"(espaço)"+sobrenome
|> nome sobrenome
```
---
# TEMPLATE STRING
- O template string é uma maneira mais otimizada de **concatenar ou unir dados** para formar uma expressão, com ele é possível misturar diferentes tipos (variáveis, textos, operadores etc) de forma mais eficiente e no final irá converter a expressão em uma **string** única
```JS
let nomeCompleto = `${nome} {sobrenome}`;
|> nome sobrenome
```
