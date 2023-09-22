#node #js #design
## Usando a função  de exportar padrão do node(commonJs)
-  habilitar para uso em outros arquivos

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

# Import e export com ES6(mais avançado)

- neste é só colocar o ``expert`` antes:

```js
export function nomefunção(..);
```
- Para exportação uma única coisa:

```js
export default {
	SOMAR,
	SUBTRAIR,
	MULTIPLICAR
	VERSÃO
};
//PARA ESSA NA HORA DE IMPORTAR TEM QUE USAR A IMPORTAÇÃO TUDO
```

- Para importar  tudo:

```js
import * as NomeDaExportação from `./localDoArquivo`;
//NomeDaExportação:qualquer nome é valido
```
- Importar apenas um modulo:

```js
import {moduloDeExportação1, moduloDeExportação2}  from `./localDoArquivo`;
```
