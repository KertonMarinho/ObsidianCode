
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
---
## COLOCANDO SINAL DE MAIS EM UMA VARIÁVEL TRASNFORMA STRING EM NÚMERO:
![[Pasted image 20231219220922.png]]

---
---
# <span style="color:red">contador </span> 
```js
const passo = 2;
let contador = 0;
contador = contador(0) + passo(2); //2
contador = contador(2) + passo(2); //4
contador = contador(4) + passo(2); //6
//igual à contador += passo
```

------
---
# <span style="color:aquamarine">Janelas do navegador</span> 
### <span style="color:yellow">Alert</span>
- lança mensagem de aviso
```js
window.alert('mensagem)';
```
### <span style="color:yellow">Janelade confirmação</span>
- Lança uma janela de confirmação no navegador
- retorna false ou true
```js
window.confirm('Deseja realmente apagar?');
```
### <span style="color:yellow">Caixa de texto</span>
- lança uma caixa de texto para usuário digitar alguma coisa
```js
window.prompt('digite seu nome:');
```

---
- Limpar console no navegador(tecla de atalho)
```console
ctrl + L
```
---
## Simplificando um Objeto
```js
function criaPessoa(nome, sobrenome, idade){
	return {
	nome:nome,
	sobrenome:sobrenome,
	idade:idade
	}
}
//Simplificado:
function criaPessoa(nome, sobrenome, idade){
	return {
	nome,
	sobrenome,
	idade
	}
}
```

---
# <span style="color:yellow">Valores Primitivos</span>
- string
- numbers
- bolean
- undefined
- null(big int,symbol)
- Dados primitivos
## <span style="color:yellow">Valores de referência</span>
- mutáveis
- Array
- object
- function
---
