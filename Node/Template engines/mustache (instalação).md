1.  No terminal:
```shell
npm install mustache-express
```
---

2.  Instale o typescript do Mustache na dependência de desenvolvimento
```shell
npm install --savedev @types/mustache-express
```
- <span style="color:brown">obs:</span> Tem que estar nas dependência de desenvolvimento no arquivo ``package.json``caso contrario pode  recorte e colar no local certo como na figura:
![[Pasted image 20231018224756.png|300]]
---
# Mustache (configuração)

1.  importando o Mustache no código:
- Lembrando que quando importar coloque os itens do node module primeiro depois os itens da aplicação.
```ts
import mustache from mustache-express;
```
![[Pasted image 20231018225321.png|300]]

---
2. No arquivo ``server.ts`` seta o mustache:
```ts
server.set('view engine','mustache');
```
- Essa linha de código define o mecanismo de visualização padrão para o aplicativo como **mustache*.
- O mecanismo de visualização é responsável por renderizar as respostas HTML do servidor
---
3. Cria uma pasta na pasta ``SRC`` chamada ``views``
![[Pasted image 20231019223005.png]]

---
4. . Seta o local da pasta da ``views``:
```ts
server.set('views', path.join(__dirname,'views'));
```
---
5. Seta a função para rodar o Mustache:
```ts
server.engine('mustache', mustache());
```
- . O método `engine` é usado para associar um mecanismo de template a uma extensão de arquivo específica
- `mustache()` é uma função que cria uma instância do Mustache como mecanismo de template. Quando você chama `mustache()`, ela retorna um objeto que pode ser usado para renderizar seus modelos Mustache. Esse objeto configurado é o que o Express utilizará para renderizar os modelos Mustache.
>[!info]
>Template, no contexto de desenvolvimento de software e design de páginas web, refere-se a um modelo ou estrutura predefinida que pode ser usada para criar documentos ou páginas consistentes e repetitivas.
>Os templates servem como um esqueleto ou estrutura básica que pode ser preenchida com conteúdo específico, permitindo criar várias instâncias de um documento com base no mesmo modelo.
---

![[Pasted image 20231019224823.png|300]]

---
6. Coloque o projeto para rodar:
```ts
npm run start -dev
```
---
7. Cria na pasta ``views`` o arquivo ``home.mustache``:
![[Pasted image 20231019225325.png]]

parou no 05:16




<span style="color:yellow"></span>



obs: Ele vem como padrão Plain text(sem cor, olhe no vscode, lado direito inferior), instale a extensão Mustache Syntax para colorir o texto( de Plain text vai mudar para mustache)

8° - Renderize o arquivo da rota
router.get('/', (req: Request, res: response)) =>{
	<span style="color:yellow">res.render('home');</span>
	
});
9° - altere as configurações json para o node monitorar mudanças no código para desenvolvimento:
No Package.json>script>start-de:
	No start-dev coloque as extensões que queira que monitore
	<span style="color:yellow">"start-dev": "nodemon -e ts, json, mustache src/server.ts</span>
	"