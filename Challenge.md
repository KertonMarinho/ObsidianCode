# <span style="color:aquamarine">Challaenge #163</span>
```js
var a = 'b';
var b = 'c';
(function() {
  console.log(a); //undefined
  var a = 'd';
  b = 'e';
  console.log(b); // e
})();
console.log(a); // b
console.log(b); //e
```
#### What is the output?
1. d e b c
2. <span style="color:yellow"> undefined e b e</span>
3. undefined e b c
4. b c d e

Este código é um exemplo do que é conhecido como "hoisting" (elevação) de variáveis em JavaScript, juntamente com escopo de variáveis.

Aqui está a explicação passo a passo:

1. `var a = 'b';` e `var b = 'c';` declaram duas variáveis globais, `a` e `b`, com os valores iniciais 'b' e 'c'.

2. Em seguida, há uma função anônima imediatamente invocada (IIFE) definida pelo `(function() {...})();`. Isso significa que o código dentro dessa função será executado imediatamente.

3. Dentro da função, há uma instrução `console.log(a);`. No entanto, aqui ocorre o fenômeno de hoisting. A declaração da variável `a` é içada (hoisted) para o topo do escopo da função, mas a atribuição `var a = 'd';` ainda não ocorreu, portanto, a variável `a` é inicializada como `undefined` neste ponto. Portanto, essa instrução irá imprimir `undefined`.

4. Em seguida, a instrução `var a = 'd';` define uma variável local `a` dentro do escopo da função e a inicializa com o valor 'd'. Esta variável `a` local sombreia a variável global `a` dentro do escopo da função, mas não afeta a variável global fora da função.

5. A instrução `b = 'e';` atualiza a variável global `b` para 'e'. Isso ocorre porque não há uma declaração de variável `b` dentro do escopo da função, então o JavaScript procura a variável `b` no escopo mais próximo, que é o escopo global.

6. A próxima instrução `console.log(b);` dentro da função imprime o valor da variável global `b`, que foi alterado para 'e' na etapa anterior. Portanto, essa instrução imprimirá 'e'.

7. Fora da função, as duas últimas instruções `console.log(a);` e `console.log(b);` imprimirão os valores das variáveis globais `a` e `b`. Como a função não afeta as variáveis globais `a`, estas instruções fora da função imprimirão 'b' para `a` e 'e' para `b`.
---
