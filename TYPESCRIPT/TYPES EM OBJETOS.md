- TYPE QUE MAIS USADO
- Para colocar um types em objeto, cria um objeto no parâmetro explicando como vai ser este objeto,vc colocar cada propriedade  dela e o tipo dela``{nome:string, idade:number}
```js
function resumo (usuario: {nome: string, idade: number}) {
	return `Ola ${usuario.nome}, tudo bem? Você tem ${usuario.idade}anos;`
}
// impementação
let u = {
	nome: 'kerton',
	idade: 21
};
resumo(u)
```
- se tiver outro objeto:
```js
...resumo(usuario: {nome: string, idade: number}, outro: {})..
//objeto1 usuario
//obejeto2 outro
```
# Propriedade opcional
- Como exemplo anterior, colocar o segundo parâmetro como opcional
```js
function resumo (usuario: {nome: string, idade?: number}) {
 if(usuario.idade !== undefined){
	return `Ola ${usuario.nome}, tudo bem? Você tem ${usuario.idade}anos;`
} else {
	return `Olá ${usuario.nome}, tudo bem?`;
}
// impementação
let u = {
	nome: 'kerton',
	idade: 21
};
resumo(u)
```
- Usa -se o ponto de interrogação no qual variável vc quer por como opcional``.. idade?: number
