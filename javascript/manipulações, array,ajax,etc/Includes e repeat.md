# Includes
- servi tanto para string, tanto para Array
- Retorna true ou false
- determina se um conjunto de caracteres pode ser encontrado dentro de outra string.
```js
let lista - {'ovo','cafe', 'arroz','feijão', 'macarrão'};
console.log(lista.includes('ovo'));
//true
let nome ='kerton';
console.log(nome.includes('b'));
//false
```

# repeat
- método de [`String`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) valores constrói e retorna uma nova string que contém o número especificado de cópias desta string, concatenadas
```js
console.log('x'.repeat(5));
//xxxxx
let nome = 'kerton';
console.log(nome.repeat(2));
//kerton kerton
```