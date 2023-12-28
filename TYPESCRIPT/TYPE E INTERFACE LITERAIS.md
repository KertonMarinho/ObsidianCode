# TYPES LITERAIS
#Chagpt 
TypeScript, os type literals são uma característica poderosa que permite definir tipos que são literalmente baseados em valores concretos. Eles permitem criar tipos que aceitam apenas valores específicos.

Por exemplo, suponha que você queira definir um tipo que aceite somente um conjunto limitado de valores para representar os status de um pedido. Você pode usar um type literal da seguinte forma:

```typescript
type StatusPedido = 'pendente' | 'processando' | 'completo' | 'cancelado';
```

Aqui, `StatusPedido` é um type literal que pode aceitar somente os valores definidos: `'pendente'`, `'processando'`, `'completo'` ou `'cancelado'`. Quando você declara uma variável com esse tipo, ela só pode conter um desses valores. Isso ajuda a garantir que o código seja mais explícito e impeça a atribuição de valores que não estão dentro desse conjunto específico.

Os type literals são úteis para criar tipos mais precisos e restritivos, tornando o código mais legível, menos propenso a erros e facilitando o trabalho com conjuntos específicos de valores em suas aplicações TypeScript.

---
<span style="color:orange">Exemplo</span>
- Dentro da variável só poderá ter o type literal que foi designado:
- Geralmente em variáveis são inúteis 
```js 
let nome: 'kerton'= 'kerton';
nome = 'kerton';
nome= 'pedro'; //error
```
---
<span style="color:orange">Exemplo</span>
- muito usado quando tem Union Types
```js
function mostrarTexto(texto: string, alinhamento: 'left' | 'right' | 'center';){...};

mostrarTexto('Kerton','left');
mostraTexto('kerton','right')
mostrartexto('kerton', 'blabla'); //error
```
---
<span style="color:orange">Exemplo</span>
- retorno específico da função
```js
function temNome(nome: string): true | false {
	 if (nome !== '') {
		 return true;
	 } else {
		 return false;
	 }
};
```
<span style="color:orange">Exemplo</span>
- Retorne um objeto(type)  e um type literal ao mesmo tempo


```js
function configurar(propos: {width: number, height: number} | 'auto'){...} 
configurar({width: 100, height: 200}); //ok
configurar('auto');  //ok
configurar('AUTOMÁTICO');  //error3
```
---
---
# INTERFACE LITERAIS
- acontece de um erro que vc colocar o type (exemplo do código 'get') mas ele identifica o error
```js
function fazerRequisitos(url: string, mrthod: 'get' | 'post') {...};
 let url = "https://google.com.br";
 let method = 'get'; //error
 fazerRequisição(url, method);
```
-  o typescript entende que ``get`` é muito fraco é precisa de melhor detalhada

- Para resolver cria um type litela somente para o get/post
```js
function fazerRequisitos(url: string, mrthod: 'get' | 'post') {...};

type Methods - 'get' | 'post';<---
															   
 let url = "https://google.com.br";
 let method = 'get'; //error
 fazerRequisição(url, method);
```
- Para objetos:
```js
function fazerRequisitos(url: string, mrthod: 'get' | 'post') {...};

type RequestDetials ={
	url: string,
	method: 'get' | 'post'
};
let req = {
	url: 'https://www.google.com',
	method: 'get'
};
 fazerRequisição(url, req.method);
```