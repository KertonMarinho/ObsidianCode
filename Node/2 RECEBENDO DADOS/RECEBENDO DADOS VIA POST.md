- Pelo Post os dados enviados não aprece na query string da url
- Para pegar os dados da requisição precisa pegar no corpo da requisição
- Todos os dados serão enviados juntos serão inseridos dentro do cabeçalho geral da minha requisição, dentro do Body(corpo da requisição)
-  Precisa mudar algumas configurações no servidor:

1. Pare o servidor de tiver funcionando(Nodemon), ctrl+s
2. no arquivo ``serve.ts``
3. Importante! Tem  que ser antes das rotas.
4. Usar o elemento ``urlencodeed``, ele habilita no corpo da requisição para que ajuste os dados para serem acessíveis dentro da rota
```ts
server.use(express.urlencoded({extended: true}));
```

![[Pasted image 20240105100015.png|500]]
5. Inicia o servidor

```shell
c:\projetos\node>npm run start-dev
```
6. No arquivo da página ``idade.mustache`` mude o método para ``post``
![[Pasted image 20240105100400.png]]
7.  Cria uma rota para o método POST
8. No arquivo ``index.ts`` cria a rota do método POST
```ts
router.post('/idade',(req: Request, res: Response)=>{
	//trasnfira tdo o código do metodo POSt menos  da visualização da página(res.render...) e apague o código que trasnferiu
	
});
```
![[Pasted image 20240105101120.png]]
09. troca  a variável booleana mostrarIdadede para <u>true</u>
10. Como foi enviado no corpo da requisição e não na query String, troque no if (``req.query.ano``) para  ``re.body.ano``
![[Pasted image 20240105101401.png|450]]
---
---
- Como está no método POST ,se tentar inserir os dados que já esteje com os dados escritos, vai aparecer está mensagens de aviso:
![[Pasted image 20240105101748.png|500x200]]
- Caso queira tirar a mensagem precisamos mudar a rota
No arquivo  da página ``idade.mustache`` coloque a função <u>Action</u> com o novo caminho escolhido
![[Pasted image 20240105102132.png|600x200]]
- Mude a rota do post para o caminho escolhido no Action no arquivo``index.ts``:
![[Pasted image 20240105102332.png|600x200]]
- agora a rota de envio é diferente da página.