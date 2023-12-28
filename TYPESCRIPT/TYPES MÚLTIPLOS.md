- tupes unidos ou types opcionais

## variável
```js
let idade: string | number = 90;
idade = document.getElementById("idade").innerHTML;
```

## funções
```js
function mostrarIdade(idade: string | idade) {
	console.log("MInha idade é ": +idade);
}
mostrarIdade(90);
mostrarIdade("90");
```

>[!warning] Cuidado quando usar mais de uma tipagem!
>Quando tem uma parâmetro que têm mais de um tipo diferente e estou utlizando uma propriedade ou uma função e que ela é exclusiva para um parâmetro, obrigatoriamente tem que verificar("if") o tipo de parâmetro dentro esta propriedade deste função..

```js
function mostrarIdade(idade: string | idade) {
	if(typeof idade ==='string') {
		console.log(idade.toUppercase());
	}else {
	console.log("MInha idade é ": +idade);
	}
}
mostrarIdade(90);
mostrarIdade("90");
```