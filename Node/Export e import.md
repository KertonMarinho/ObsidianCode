#node #js #design
## Usando a função  de exportar padrão do node(commonJs)
: habitar para uso em outros arquivos

1. exporte o que vc quer exportar
 
```node
module.export.somar = somar;
```
>[!note]
> . vc pode exportar string, functions, etc.
>. somar recebe a função somar
>. vc pode escrever a propria função:
> 	'module.export.somar=function();'

2. para importar:
 
```js
const nomeVariável = require('./nomeDoArquivo')
//não precisa .ts
```
Para usar:

```js
	matematica.somar();
```

# import e export com ES6(mais avançado)

