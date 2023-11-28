# Data completa internacional
```js
let d = new date();
console.log(d);
//wed sep 11 2019 07:59:39 gmt-300 (horáriode Brasília)
```
ou
```js
let d = new date();
console.log(d.toString);
//wed sep 11 2019 07:59:39 gmt-300 (horáriode Brasília)
```
# Data resumida
```js
let d = new date();
console.log(d.toDateString());
//wed sep 11
```

# Horário oficial de greenwitch
```js
let d = new date();
console.log(d.toUTCString);
//wed sep 11 2019 07:59:39 gmt
```

# Determinar a hora como parâmetro
- Lembrando que no Js o mês começa no Zero(Janeiro = 0, fevereiro = 1,...)
```js
let d = new date(2022, 0 ,1 ,12, 30, 12);
console.log(d.toStrring);
//wed Jan 01 2020 12:30:39 gmt-300 (horáriode Brasília)
```
- pode por o parâmetro com formato DateString
```js
let d = new date('2020-01-01 15:42:17');
console.log(d.toString);
//wed Jan 01 2020 15:42:39 gmt-300 (horáriode Brasília)
```
- pode somente por o ano e mês:
```js
let d = new date('2020, 2');
console.log(d.toString);
//wed mar 11 2020 07:59:39 gmt-300 (horáriode Brasília)
```
# Data inicial do Javascript
- O Js começa a contar os milissegundos a partir de 01/jan/1970
```js
let d = new date(0);
console.log(d.toUTCString);
//Thu Jan 01 1970 00:00:00 gmt
```
# Data com parâmetro milissegundos
```js
let d = new date(123156646);
console.log(d.toUTCString);
//fri, 02 Jan 1970 10:12:36 GMT
```

- Em milissegundos em negativos mostra data antes de 1970:
```js
let d = new date();
console.log(d.toUTCString);
//tue, 30 Dec 1969 13:47:23 GMT
```
---
# Pegar somente o ano da data
```js
let d = new date();
let nonoValor = d.getFullYear();
console.log(novoValor);
//2019
```

# Pegar somente o mês
```js
let d = new date();
let nonoValor = d.getMonth();
console.log(novoValor);
//8 (lembrando que o mês começa no zero)
```

# Pegar o dia da semana
`` a semana começa no zero(domingo)
```js
let d = new date();
let nonoValor = d.getDay();
console.log(novoValor);
//3 => quarta-feira
```
# Pega o dia
```js
let d = new date();
let nonoValor = d.getDate();
console.log(novoValor);
//11
```
# Pega a hora
```js
let d = new date();
let nonoValor = d.getHours();
console.log(novoValor);
//8
```
# Pega os minutos
```js
let d = new date();
let nonoValor = d.getMinutes();
console.log(novoValor);
//17
```

# Pega os segundos
```js
let d = new date();
let nonoValor = d.getSeconds();
console.log(novoValor);
//27
```
# Pegar os milisegundos
```js
let d = new date();
let nonoValor = d.getMilliseconds();
console.log(novoValor);
//631
```
# Pegar o Time stanp
- Quantidades de milissegundos desde 1970
```js
let d = new date();
let nonoValor = d.getTime();
console.log(novoValor);
//1568200763622
```
# Pegar o horario atual em time stamp sem definir uma variável
- Retorna o Time stamp do momento atual
```js
let d = new date();
let nonoValor = d.date.now();
console.log(novoValor);
//1568200763622(fica atualizando)
```