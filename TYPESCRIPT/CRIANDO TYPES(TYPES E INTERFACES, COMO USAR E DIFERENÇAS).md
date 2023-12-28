- Usa se ``type <nome da type criada> = string
- Usa-se PascalCase (todo nome começa com letra maiúscula)
- Usa-se apenas em duas situações
		1. quando quer simplificar o código(repetição de códigos)
		2. quando o type é replicável em outros locais do código

----
<span style="color:orange">Exemplo</span>
```js
type Idade = string| number;

let idade: idade = 90;

function mostrar(i: idade){...};
//também no retorno
function mostrar(i: idade): Idade{...};
```
<span style="color:orange">Exemplo</span>
- Geralmente usa-se mais em objetos:
- quando tem muita tipagem
```js
type User  = {
	nome: string,
	idade: number
};
function resumo(usuario: user) {
	return `Ola ${usuario.nome}, você tem ${usuario.idade} anos`; 
}
resumo({
	nome: 'kerton',
	iade: 90
})
```
# FORMA DOIS DE CRIAR TYPE(INTERFACE)

```js
interface User {
	nome: string,
	idade: number
};
function resumo(usuario: user) {
	return `Ola ${usuario.nome}, você tem ${usuario.idade} anos`; 
}
resumo({
	nome: 'kerton',
	iade: 90
})
```
>[!info]
>Type quase uma variável, com o type ele não é alterável, não tem como adicionar propriedades novas
>Interface é quase uma função, interface consegue adcionoar propriedade

### Exemplo de interface alteravel
```js
interface User {
	nome: string
};
//adicionando:
interface User{
	idade: number
}
function resumo(usuario: user) {
	return `Ola ${usuario.nome}, você tem ${usuario.idade} anos`; 
}
resumo({
	nome: 'kerton',
	iade: 90
})
```