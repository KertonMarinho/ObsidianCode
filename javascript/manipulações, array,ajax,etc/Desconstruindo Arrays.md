- diferente do objeto que tem o nome como referencia array tem o índice.
- Na hora que desconstruir precisa dar um nome, pois virará uma variável
```js
let info = ['kerton Marinho', 'kerton', 'Marinho' '@kerton'];
let [nomeCompleto, nome, sobrenome, instagram ] = info;
console.log(nomeCompleto, nome, sobrenome, instagram);
//kerton Marinho, kerton, marinho, @kerton
```
# Pegar duas variáveis do array com intervalos entre elas
- Utiliza os espaços entre elas
```js
let [ nomeCompleto, , , instagram] = info;
console.log(nomeCompleto, instagram);
//Kerton Marinho @kerton
```

# criando o Array e automaticamente desconstruido ele
```js
let[nome, sobrenome] = [ 'kerton', 'Marinho'];
```
- Raramente usado

# definir uma valor padrão para desconstrução do Array
```js
let[nome, sobrenome, idade=90] = [ 'kerton', 'Marinho'];
console.log(nome, sobrenome, idade);
//kerton marinho 90

```

# desconstruindo com função
```js
function criar(){
	return [1, 2, 3];
}
let numeros = criar();
let [a ,b, c] = numeros;
console.log(a, ,b ,c;
```
- outro modo;
```js
function criar(){
	return [1, 2, 3];
}

let [a ,b, c] = criar();
console.log(a, ,b ,c;
```