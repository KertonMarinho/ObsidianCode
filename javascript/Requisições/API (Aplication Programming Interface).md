- Forma de fazer uma comunicação entre um software e outro software.
- existe alguns padrões de como JSON ou mais antigo XML

# <span style="color:green">JSON</span>
- Javascript Object Notation
- Existe uma Api fake para testar e protótipar as coisas
  [JSONPlaceholder - Free Fake REST API (typicode.com)](https://jsonplaceholder.typicode.com/)
  ![[Pasted image 20231103113301.png|300]]
  - no Json pode ter informação dentro de informação:
```json
`let pessoa = {
	nome: 'Kerton',
	idade: 41,
	características: ['sorridente','maravilhoso','top']
};`
```
 -  no Json poder armazenar objetos:
```json
`let pessoa = {
	nome: 'Kerton',
	idadde: 41,
	estetica: { `//obejeto
		`altura: 900,
		peso: 10
	}
}`
```
  