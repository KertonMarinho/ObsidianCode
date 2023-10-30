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
---
``get = pegar
``set = colocar``
# GETTER AND SETTER

1. **Get**: Um método com o prefixo **get** é usado para **retornar um valor** associado a uma propriedade. Quando você acessa essa propriedade, o método **get** é chamado automaticamente e retorna o valor desejado. É como se fosse uma leitura da propriedade.
    
2. **Set**: Um método com o prefixo **set** é usado para **atribuir um valor** a uma propriedade. Quando você define o valor dessa propriedade, o método **set** é acionado automaticamente, permitindo que você atualize o valor da propriedade. É como se fosse uma escrita na propriedade.
```js
class Person {
	_age = 0;
	steps = 0;

	constructor(name) {
		this.name = name;
	}
	takeAstep(){
		this.steps++;
	}
	get age() {   //Se cria um Get como se fosse  uma função
		return this._age;  //get retorna o valor que vc quer
	}
	set age(x){  //o set e para setar o valor da variável(modifica-la)
		this._age = x;
	}
}
let p1 = new Person('João');
let p2 = new Person('Maria');
let p3 = new Person('Pedro');

p1.Age(20); //modificando o valor da propiedade usando a função set

console.log(`${p1.name} tem {p1.age}`); // o age esta pegando a função get em vez da propriedade age
//João tem 20 anos
```
- Quando usamos set e Get colocamos um underline na propriedade do objeto``_age = 0;
- Se cria um Get como se fosse  uma função
- Get usa como fosse uma variável  sendo que ela é uma função
--- 
# CLASSES: VARIÁVEL OU MÉTODO ESTATÍCO
- ``VARIÁVEL STATIC`` está associada com a classe pessoa mas não está associada com objeto/estância que for criada. 
```JS
class Person {
	static hands = 2;
	age = 0;

	construtor(name) {
		this.name = name;	
	}
	sayHi() {
		console.log(`Oi, eu sou ${this.name} e tenho ${Person.hands} mão.`)
	//person.hands não faz refêrencia a pessoa mais uma raça de pessoa abstrata
	}
}
let p1 = new Person("Kerton");
p1.sayHi(;
//Oi, eu so Kerton e tenho duas mãos
```
- A função static ela é independente e tudo que tem dentro dela também é independente
---
# CLASSES: FACTORY
- Factory cria uma instância ou objeto do que aquilo que quero criar
```js
class Person {
	age = 0;
	constructor(name){
		this.name = name;
	}
}
function createPerson(name, age){
	let p = new Person(name);
	p.age = age;
	return p;
}
let p1 = createPerson('kerton',90);
console.log(`${p1.name} tem ${p1.age}anos.`);
//Kerton tem 90 anos
```

---
# PROGRAMAÇÃO FUNCIONAL (OU O CORRETO PROCEDURAL)
- SERIES DE FUNCÕES SE COMUNICANDO ENTRE SI PARA GERAR OBJETOS
# <span style="color:yellow">Funcional: Factory</span>

- cria funções que cria objetos
```js
function createPerson (name,lastName, age){
	return {
		name,
		lastName,
		age
	}
}
let person1 = createPerson('kerton', 'marinho', 41);
let person2 = createPerson('Daniela', 'Fulano', 20);

console.log(person1.name);
```

---
# <span style="color:yellow">Funcional: Instância e This</span>
- Na programação estrutural não tem classes mais tem funções
```js
let person = {
	name: 'Kerton',
	lastName: 'Marinho',
	age:90,
	getFullName() { //A função só funciona o this nesse formato
		return `${this.name} ${this.lastName}`;
	}
}
console.log(person.getFullName());
```
---
# <span style="color:yellow">Funcional: Construtor</span>

- Como não temo uma função construtor no funcional vc pode substituir o construtor pela uma função no próprio objeto.``Função start, por exemplo.

```js
let person = {
	name: 'Kerton',
	lastName: 'Marinho',
	age:90,
	getFullName() { //A função só funciona o this nesse formato
		return `${this.name} ${this.lastName}`;
	}
	start() {
		console.log('deu start na pessoa');
	}
}
person.start();
```

>[!warning]
>Resumindo objetos não tem construtor, só classes tem o construtor.

----
## <span style="color:yellow">FUNCIONAL HERANÇA</span>
- Cria um generalista e depois herda tudo no específico
```js
const defaultUser{  //generalsita
	name: '';
	email:´´;
	level:1;
}
const user1{  //herda tudo do defaultUser,vc pode modificar ele
	...default: 'Kerton';
	email:  'suporte@b7web.com.br'
}
console.log(user1);
```
