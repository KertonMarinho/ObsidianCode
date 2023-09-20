1°- No terminal:
<span style="color:yellow">c:\...>npm install mustache -express</span>

2°- Instale o typescript do Mustache
<span style="color:yellow">c:\...>npm install --savedev @types/mustache-express</span>

3° - importando o Mustache no código:
<span style="color:yellow">import mustache from mustache-express;</.span>

4° - configuração:
no arquivo server.ts, logo depois do servidor(inicialização do express)
<span style="color:yellow">server.set('view engine','mustache' );</span>
<span style="color:yellow">server.set('views', path.join( __ _dirname, 'views'));</span>

5° - para usar:
no server.ts
<span style="color:yellow">server.engine('mustache',mustache());</span>

6° - inicia de novo o projeto
<span style="color:yellow">npm run start -dev</span>

7° - Em viewa, cria o arquivo home.mustache

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