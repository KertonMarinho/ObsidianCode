- Quando não tiver nada para exibir execute isso.
1. NO arquivo``hoem.mustache``
2. Utiliza como um else o acento ``^``
```html
<ul>
	{{#fraseDoDia}}
		<li>{{.}}</li>
	{{/frasesDoDia}}
	{{^frasesDoDIA}}
		Não há frases motivacionais hoje
	{{/frasesDoDia}}
</ul>
```
