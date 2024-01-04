- Conteúdo parcial: se cria views específicos para pasta específica dentro da página
- Separa os layouts em arquivos diferentes
- Você pode reutilizar estes layouts em diferentes locais do site

<span style="color:orange">Exemplo</span>
1. Crias Views de uma página contato e sobre
 ![[Pasted image 20240103221447.png]]
2. Copie o corpo do arquivo nas duas páginas criadas
![[Pasted image 20240103221615.png|300]]
3. Modifique o caminho da rota contato no render  no arquivo ``index.ts`` para a rota do arquivo``contato.mustache`` :
```ts
router.get('/contato', (req: Request, res: Response)=>{
	res.render('contato');
});
```
4. Modifique o caminho da rota sobre no render  no arquivo ``index.ts`` para a rota do arquivo``sobre.mustache`` :
```ts
router.get('/sobre', (req: Request, res: Response)=>{
	res.render('sobre');
});
```
5. Agora começa o conteúdo parcial
6. Cria a pasta partials
![[Pasted image 20240103222338.png|200]]
7. Cria Views específicos para áreas específicas dentro  do site
8. Cria dentro da pasta``partials`` o arquivo ``header.mustache``
![[Pasted image 20240103222617.png|200]]
9. Transfira o corpo do html do arquivo ``home.mustache`` para  o arquivo``header(cabeçalho)``
![[Pasted image 20240103222818.png|300]]
10. Apague o corpo que foi transferido para pasta header e coloque o caminho do mustache:
``{{>partials/header}}``, faça isso nas paginas home, contato e sobre.

![[Pasted image 20240103223057.png|300]]

---
11. Cria o rodapé da pagina também:
12. Cria outra pasta no partials chamado``footer.mustache``
![[Pasted image 20240103223444.png|200]]
13. Adicione o corpo que vai ser o rodapé, fechando o body e o html nas págianas home, contato e sobre:
![[Pasted image 20240103223544.png]]
14. Acrescente o caminho da rota``{{>partials/footer}}`` nas páginas home, contato e sobre
 ![[Pasted image 20240103223814.png]]
---
---
- Para criar uma página enxuta, podemos criar uma arquivo somente para uma lista de produtos
- Em vez de deixar o código da lista no home:
![[Pasted image 20240103224247.png|280]]
1. Cria em ``partials`` o arquivo ``productItem.mustache````
![[Pasted image 20240103224824.png|200]]

1. Coloque a rota da lista neste arquivo criado
![[Pasted image 20240103224527.png]]
3. no arquivo``home.mustache`` coloque a rota do arquivo ``productItem``
![[Pasted image 20240103224728.png]]
---
---
- Para otimizar o código:
1. cria um arquivo em views chamado``pages``
2. Coloque as páginas nesta página
![[Pasted image 20240103225217.png|200]]
3. Agora corrija o endereço  da rota no arquivo ``index``
![[Pasted image 20240103225424.png|400]]
![[Pasted image 20240103225611.png|300]]


