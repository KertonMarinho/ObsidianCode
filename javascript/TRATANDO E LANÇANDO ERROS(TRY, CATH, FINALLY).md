- A declaração `try` consiste em um bloco `try`, que contém uma ou mais declarações, e ao menos uma cláusula `catch` ou uma cláusula `finally`, ou ambas. Ou seja, há 3 formas de declarações `try` :
# <span style="color:red">try/cath</span> 
- As declarações **try...catch** marcam um bloco de declarações para testar (**try**), e especifica uma resposta, caso uma exceção seja lançada.
- Significa tente executa o est código, caso contrario execute o próximo.
```js
try {
	console.log(naoExisto);
} catch(err) {
	console.log('naoExixto não existe.');
	console.log(err); //exibe o error que aconteceu
}
```
![[Pasted image 20240102085024.png|450]]
<span style="color:orange">Exemplo</span>
```js
function soma(x,y) {
	if (typeof x !== 'number' || typeof y !== 'number') {
	throw new Error('x e y precisam ser números.')
	}
	return x +y;
}
try {
consoloe.log(soma(1,2));
console.log(soma('1',2));
} catch(error) {
	console.log(error); 
}
```
resposta:
![[Pasted image 20240102090843.png|400]]

>[!throw]
>* A **declaração** **`throw`** lança uma exceção definida pelo usuário. A execução da função atual vai parar (as instruções após o `throw` não serão executadas), e o controle será passado para o primeiro bloco [`catch`](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/try...catch) na pilha de chamadas. Se nenhum bloco `catch` existe entre as funções "chamadoras", o programa vai terminar.
>Use a instrução `throw` para lançar uma exceção. Quando você lança uma exceção, `expressão` especifica o valor da exceção. Cada uma das intruções a seguir lança uma exceção:
>> throw new Error : Função construtora padrão do JS que lança erro padrão do JS
>```
throw "Erro2"; // gera uma exceção com um valor string
throw 42; // gera uma exceção com o valor 42
throw true; // gera uma exceção com o valor true```

----

# <span style="color:red">Bloco Finally</span> 
```js
try{...}
catch(e) {
//É executada quando há erros
} finally {
//SEMPRE É EXECUTADA
}
```
- Finally é um trecho do try/cathc que sempre será executado.
- Pode ter um try dentro do outro try para deixar mais limpo o código:
![[Pasted image 20240102092139.png|500]]







