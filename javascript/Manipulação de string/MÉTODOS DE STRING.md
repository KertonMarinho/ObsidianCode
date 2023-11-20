# LENGTH
- A propriedade `length` de um objeto [`String`](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/String) contém o comprimento da string. 
- Quantos caracteres tem na string
```js
str.length
```
---
# indexOf()
- retorna a posição em do texto onde se encontra  na string
- O método `indexOf()` retorna o índice da primeira ocorrência do valor fornecido em searchValue, começando a busca a partir de `fromIndex`. Retorna `-1` se o valor não for encontrado.
- Se achar uma coisa ele da a posição que se encontra a string
```js
let resultado = nome.indexOf('b');
//0
```
---
# Métodos de extrair informações de string
## <span style="color:violet">Slice()</span> 
- ``slice(posição inicial,posição final(opcional))
- Se usar a posição inicial ele vai pegar da posição inicial até o restante
- O método `slice()` extrai uma parte de uma string e a retorna como uma nova string, sem modificar a string original.
- O Slice pode paegar a string ao contrário``.slice(-4);
```js
let resultado = nome.slice(0);
```

## <span style="color: #1E90FF">Substring</span>
- O método `substring()` retorna a parte da string entre os índices inicial e final, ou até o final da string.
- Igual ao slice
- Substring só começa pelo padrão'
```js
str.substring(indexStart[, indexEnd])
```

## <span style="color:red">substr</span> 
- ``str.substr(posição inicail,quantidades de caracetes )
- 90% dos casoas subrt vai funcioanar
- aceita números negativos

## <span style="color:aquamarine">Replace</span> 
- ``replace(pesquise por x, subdtitua por y)
 ```js
 let nome = 'eu gosto de carros';
 let resultado = nome.replace('carros','motos');
 console log(resultado);
 //Eu gosto de motos
```

## <span style="color:#BC8F8F">toUpperCase</span>
- colocar toas as palavras em letra maiúscula.
```js
let resultadoi = nome.toUpperCase();
```

## <span style="color:#6959CD">toLowerCase</span>
- Colocar tudo em minúsculo:
```js
let resultado = nome.toLowerCase;
```

## <span style="color:#7FFFD4">Concat</span>
- concatena duas strings
- meio inútil
```js
let nome= 'kerton';
let resultado = nome.concat('Marinho');
cosole.log("resultado: ", resultado);
```

## <span style="color:#FF1493">Trim</span>
- Tira todos os espaços de um campo ou string
```js
let resultado = nome.trim();
```

## <span style="color:#DC143C">charArt()</span> 
- retorna qual caractere está em determinada posição
```js
lel resultado = nome.charArt(3);
```
>[!info]
>Apartir da versão cinco ecmarScriprt usa-se desse modo:
>let resultado = nome[2];

## <span style="color:#FFFF00">split</span>
- divida uma string em um Array(trasnforma uma string em um Array)
``.split(parametro de separação:/,(espaço),etc)
```js
let resultado = nome.split('/');
```
---
# METODOS DE NUMBERS
