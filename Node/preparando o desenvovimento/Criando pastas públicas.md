1. primeiro cria a pasta pública 
![[Pasted image 20231015220124.png|100]]
- pasta que têm acesso público
2. dentro da pasta publica cria a pasta CSS e images
![[Pasted image 20231015220311.png|100]]
3. torne a pasta publica no ``server.ts`` estática 
	- Express transforma ela acessível ao navegador(url)
```ts
server.use(express.static('public'));
```
![[Pasted image 20231015220905.png|300]]
4. cria uma rota especifica para ter os arquivos estáticos<sub>(ignore este item)</sub>:
```ts
server.use('/static', express.static('public'));
//geralmente não usamos prefixos(/static)
```
5. Define um caminho absoluto para que não der erro de página não encontrada, para definir o caminho inteiro até a pasta ``public``
	- importa a biblioteca ``path`` :
	```ts
	import path from 'path';
```
	- define o caminho de execução e o local da pasta ``public``:
	```ts
	server.use(express.static(path.join(__dirname,'.../public')));
	//--dirname,específica o diretório que está sendo executado
	//..., significa que tem que voltar uma pasta para acessar a pasta public
```