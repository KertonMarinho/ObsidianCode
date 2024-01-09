# <span style="color:orange">Exemplo de uso do Mustache</span>
- Vamos renderizar a página, que há página diga ``opa, tudo bem (nome da pessoa)``.
- 
### <span style="color:yellow">Passos:</span>
1. Cria uma variável com o nome da pessoa no arquivo``index.TS``
```ts
router.get('/', (req: Request, res: Response)=> {
	let user: string = 'Kerton';
	res.render('home',{ user});
});
//outro jeito:
router.get('/', (req: Request, res: Response)=> {
	let user: string = 'Kerton'
	res.render('home',{ user: 'Pedro'})
});

//o render têm dois parâmetros principais
//render(nome do views que quer chamar,objeto com informaçoes que quer enviar)
```
2. No arquivo ``home.mustache`` acrescente o nome do usuário``{{ user}}``:
![[Pasted image 20240103120346.png|300]]
---
- Podemos por um objeto para renderizar:
 ![[Pasted image 20240103120730.png|300]]
. Para chama-lo no arquivo ``home.mustache``
![[Pasted image 20240103120848.png|360]]
- se quiser pode criar direto na função Render:
![[Pasted image 20240103121120.png|360]]
- <span style="color:red">obs: </span> Lembrando para que as informações apareçam têm que ser mandado o nome da variável ou objeto(desconsiderando se já está escrito nome/value no render) no ``Render``.







