#node #js #design
-  Há duas formas de exportar e importa entre arquivos do projeto node no node(habilitar funções, string e etc para outros arquivos)
# <span style="color:yellow">Import/Export em Commonjs</span>

1. exporte o que vc quer exportar no arquivo ``index,ts``
 - Geralmente no final do arquivo
```node
module.export.somar = somar;
```
>[!note]
> . vc pode exportar string, functions, etc.
>. somar recebe a função somar
>. vc pode escrever a propria função:
> 	'module.export.somar=function();'

2. para importar:
 - Coloque no início do arquivo
```js
const nomeVariável = require('./nomeDoArquivo')
//não precisa .ts
```
Para usar:

```js
	matematica.somar();
```
---
---

# <span style="color:yellow">Import /export com ES6(mais avançado)</span>
- uso mais moderno
- neste é só colocar o ``expert`` antes da variável, funções, etc ,que v c queira exportar

```js
//Função
export function nomefunção(..);
//Variável
export versao: string = '1.0';
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
- Importar apenas um modulo:

```js
//import{o que vc quer imortar} from `./local do arquivo`
import {moduloDeExportação1, moduloDeExportação2}  from `./localDoArquivo`;
```
- Para importar  tudo:

```js
//import *(tudo) as <nome qualquer para chamar> from `./<local>`
import * as NomeDaExportação from `./localDoArquivo`;
//NomeDaExportação:qualquer nome é valido
```
- Importar apenas um modulo:

```js
//import{o que vc quer imortar} from `./local do arquivo`
import {moduloDeExportação1, moduloDeExportação2}  from `./localDoArquivo`;
```
