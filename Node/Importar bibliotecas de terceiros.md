- Neste site vc pode usar diversas bibliotecas de terceiros
- npmjs.com/package/

## instalar biblioteca de terceiros

```shell
npm install <nomeDaBiblioteca>
```
---
- aqui se concentra as dependências do projeto(bibliotecas)
	
	![[Pasted image 20230922232056.png|350]]
---
- Como vc usa  a bibliotecas:
```js
import matematica from `validator`;
//sem barra)(./) significa que estra na pasta nodemodulos
```
---
- vc pode instalar o types da biblioteca
![[Pasted image 20230922232650.png|300]]
``DT significa que essa biblioteca tem o typescript declaration
- Para instalar:
	
```shell
npm install --save-dev @types/<nomeDaBiblioteca>
//--save--dev - salvo somente na area de desenvolvimento
```
