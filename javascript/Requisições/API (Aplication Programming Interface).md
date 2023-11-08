- Forma de fazer uma comunicação entre um software e outro software.
- existe alguns padrões de como JSON ou mais antigo XML

# <span style="color:green">JSON</span>
- Javascript Object Notation
- Existe uma Api fake para testar e protótipar as coisas
  [JSONPlaceholder - Free Fake REST API (typicode.com)](https://jsonplaceholder.typicode.com/)
  ![[Pasted image 20231103113301.png|300]]
  - no Json pode ter informação dentro de informação:
```json
let pessoa = {
	nome: 'Kerton',
	idade: 41,
	características: ['sorridente','maravilhoso','top']
};
```
 -  no Json poder armazenar objetos:
```json
let pessoa = {
	nome: 'Kerton',
	idadde: 41,
	estetica: { `//obejeto
		`altura: 900,
		peso: 10
	}
}
```
  ---
# <span style="color:aquamarine">JSON.parse</span>
- O método **`JSON.parse()`** analisa uma string JSON, construindo o valor ou um objeto JavaScript descrito pela string
  -  Pega a string json e transforma em um json real(objeto real)
  - A palavra ``json`` têm que estar em letra maiúscula.
  - Basicamente vira um objeto
 ![[Pasted image 20231105224822.png|400]]

---
## <span style="color: #00FF00">Json.stringify</span>
- Inverso da função parse
- Passa um json e transforma em uma string
- Basicamente-se transforma em uma string
- ![[Pasted image 20231106224441.png|350]]
---
<span style="color:orange">Exemplo</span>
![[Pasted image 20231106224648.png|400]]

---
> [!SUMMARY] stringify x parsen
> Parse = pegar uma string e trasnforma em json
> stringfy = Pega um json e trasnforma em string


