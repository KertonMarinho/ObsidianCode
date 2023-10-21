# Conceitos
### <span style="color:yellow">Programação Orientada a objetos</span>
- Sigla (POO-OOP)

### <span style="color:yellow">Programação Procedural</span>
- Códigos executados de cima para baixo(Em sequência)
- Javascript e uma linguagem precedural (Prototype-based procedural language),mas Js aceita tanto POO quanto Funcional

### <span style="color:yellow">Programação Funcional</span>
- Sigla em inglês FP
- Finctional Programming Paradigm
---
# CLASSES: CONSTRUTORES E THIS
-  Todo objeto tem características e ações que ele pode executar
### <span style="color:yellow">Construtor</span>
- O construtor é um método especial para criar e inicializar um objeto criado a partir de uma classe.
- Ela vai ser executada sempre que for criada por exemplo uma pessoa nova
```js
class Person{
	constructor(name,age) {
		this.name=name; //thos representa o próprio objeto criado
		this.age = age;
		}
}
```
---
# Instânciando classes
```js
class person...
}
//objecto...instâncias
let p1 = new person("joào"); //no caso do construtor o this seria p1
//para trocar o nome da propriedade da classe
p1.person = "maria";

```
---
# classes: Action
- Cria ações que usuário pode fazer
```js
class Person {
	age = 0;
	steps = 0;

	constructor(name) {
		this.name = name;
	}
	takeAstep(){
		this.steps++;
	}
	steAge (newAge){
		this.age = newAge;
		} else {
			console.log('idade não aceita.('só números)')};
	}
}
let p1 = new Person('João');
let p2 = new Person('Maria');
let p3 = new Person('Pedro');

p1.setAge(20);

console.log(`${p1.name} tem {p1.age}`);
//João tem 20 anos
```
