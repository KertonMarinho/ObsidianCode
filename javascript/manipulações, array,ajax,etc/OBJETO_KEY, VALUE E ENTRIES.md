(funciona tanto em arrays como objetos)

# <span style="color:salmon">keys</span> 
- Pegar as chaves do array
```js
let lista = ['ovo', 'macarrão', 'feijão', 'pipoca'];
console.log(object.keys());
//(4) ["0", "1","2", "3"]
```

# <span style="color:pink">values</span> 
```js
let lista = ['ovo', 'macarrão', 'feijão', 'pipoca'];
console.log(object.values());
//['ovo', 'macarrão', 'feijão', 'pipoca'];
```

# <span style="color:purple">entries</span> 
-  método estático retorna uma matriz dos pares enumeráveis ​​de valores-chave de propriedade com chave de string de um determinado objeto.
```js
let lista = ['ovo', 'macarrão', 'feijão', 'pipoca'];
console.log(object.entries());
```
![[Pasted image 20231218223839.png|400]]
- EM OBJETOS:
```JS
LET PESSOA = {
	NOME: 'kerton',
	sobrenome: 'marinho',
	idade: 90
};
console.log(object.keys(pessoa));
```