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
### <span style="color:yellow">Instânciando classes</span>
```js
class person...
}
//objecto...instâncias
let p1 = new person("joào"); //no caso do construtor o this seria p1
//para trocar o nome da propriedade da classe
p1.person = "maria";

```