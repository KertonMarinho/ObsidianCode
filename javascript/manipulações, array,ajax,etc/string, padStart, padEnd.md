# <span style="color:#20B2AA">padEnd</span>
- Parâmetro:
	``padEnd(quantas string tem quer ter obrigatoriamente,qual item colocar caso não esteja em x itens obrigatórios);
-  método de [`String`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) valores preenche esta string com um determinado string (repetida, se necessário) para que a string resultante atinja um determinado comprimento. O preenchimento é aplicado a partir do final desta string.
```js
let telefone = '54';
console.log(telefone.padEnd(5,'x'));
//54xxx
```

# <span style="color: #1E90FF">padStart</span>
- o mesmo que padEnd,mas o preecnhimento será antes da string
```js
let telefone = '54';
console.log(telefone.padStart(5,'x'));
//xxx54
```