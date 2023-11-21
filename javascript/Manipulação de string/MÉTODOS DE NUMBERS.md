# <span style="color:salmon">toString()</span> 
- Trasnformar números em strings
```js
let n = 10;
let res = n.toString();
console.log(res);
//10(color preto indicando string, se fosse númeor seria azul no console)
```

# <span style="color:green">tofixed()</span> 
- arredonda um numero decimal
- Parâmetro desta função indica quantas casa decimais depois da vírgula
```js
let n = 10.654657264;
let res = n.toFixed(2);
console.log(res);
//10.65
```
# <span style="color:red">parseInt()</span> 
- Transformar uma string em um número
```js
let n= '25';
let res = parseInt(n) + 5;
console.log(res);
//30
```

# <span style="color:yellow">parseFloat</span>
- Ao contrario do parseInt, parseFloat preserva a casas decimais
```js
//com parseInt
et n= '25.9';
let res = parseInt(n) + 5;
console.log(res);
//30
//com parsefloat
et n= '25';
let res = parseFloat(n) + 5;
console.log(res);
//30.9
```
>[!info]
>Usando parseFLoat e toFixed ao mesmo tempo
>let = 50.589799
>console.log(parseFloat(x).toFixed(3));

>[!warning]
>Usando o  number no lugar do parseInt epreservou o numero mesmo sendo um float
>let num1 ='10.5';
>let num2 =5;
>let res = number(num1)+num2
>coonsole.log(res);
>//11



