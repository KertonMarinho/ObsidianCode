npm initNa pasta criada do projeto:
inicia o npm(gerenciador de pacotes)

```shell
npm init
```

**Ele vai perguntar :**

<mark style="background: #FFB86CA6;">Package name:</mark>(node): Nome do projeto, ele já vem com o nome da própria pasta do projeto, de enter se não quiser modificar
<mark style="background: #FFB86CA6;">version:</mark>
<mark style="background: #FFB86CA6;">description:</mark>
<mark style="background: #FFB86CA6;">Entry point:</mark>(index.js) arquivo principal
<mark style="background: #FFB86CA6;">teste command:</mark>
<mark style="background: #FFB86CA6;">git repository:</mark>
<mark style="background: #FFB86CA6;">Key word:</mark> palavras chaves
<mark style="background: #FFB86CA6;">author:</mark>
<mark style="background: #FFB86CA6;">license(isc):</mark>

<mark style="background: #FFB86CA6;">is this ok ?</mark>yes

**você pode configurar automaticamente:**
```shell
c:\projetos/node>npm init -y
```


<h1>Instalando o Typescript</h1>
<mark style="background: #ABF7F7A6;">1°</mark>instale globalmente o typescript ( caso não esteja instalado em sua máquina)

```shell
npm install -g typerscript
```
<mark style="background: #ABF7F7A6;">2°</mark> - inicia um arquivo de configuração do typescript do nosso projeto

```shell
tsc --init
```
<sub>ele cria um arquivo chamado <mark style="background: #ABF7F7A6;">tsconfig.json</mark></sub>

```
Monte a estrutura da pasta do nosso projeto
-  Cria a pasta src(significa código fonte) onde o typescript vai ficar
-  cria o arquivo ''index.ts'' no src
-  Cria a pasta dist(siginifca distribuição) onde o javascript vai ficar
```

> Antes(caso não funcione, [[2 habilitar no shell do windows para rodar script]] "set-ExecutionPolicyRemoteSigned)


agora para gerar o arquivo index.ts no dist #5
****
<h2> Configurando a typescript</h2>

*  Na pasta <u>tsconfig.json</u> modifique o arquivo <span style="color:green">"target":"es5" </span>para o <span style="color:green">"target":"es6" </span>.
* Des comentar o ``moduleResolution`` na pasta ``tsconfig`` no grupo Modules
![[Pasted image 20240106090654.png]]
 
 * Defina e descomente no arquivo ``tsconfig.json`` no grupo ``Modules``em <span style="color:green">rootDir </span> a pasta do projeto(<span style="color:green">"rootDir":"./src" </span>)
 
 ![[Pasted image 20240106091232.png]]
 
 * Defina  e descomente no arquivo <u>tsconfig.json</u> no modulo ``Emit``em <span style="color:green">outDir </span> a pasta de destino do projeto(<span style="color:green">"ouDir":"./dist" </span>)
 ![[Pasted image 20240106091446.png]]
 
  
 - instale uma dependência chamada <u>types/node</u> (traz ao typescript novas noções de código, ex.autocomplit)
 
```shell
npm install --save-dev @types/node
```
``--save-dev, porque só usaremos essa biblioteca no desevonvimento`

>[!note]
> Essa biblioteca cria uma pasta chamada <u>node_modules</u> , com o tempo essa pasta fica pesada, não recomenda subir no GitHub essa pasta, você pode até apagar ela, quando baixar de novo para sua máquina de um comando no terminal ``npm install`` (como está na dependência no Node``package.json``, o Node automaticamente baixa ela de novo)

- Faça o typescript monitore o código para que ele crie o respectivo código na pasta de distribuição``dist``:
	1. Inicia o watching mode (comando que  fax o node monitorar qualquer mudança do código)
	
	```shell
tsc -w
```
    2. Abra outro terminal
    3. Execute o node no arquivo que vc que ele executa
    
```Shell
	node dist/index.js
```
	``agora ele vai rodar o código ts em js``

----
# CRIANDO UM SCRIPT COM NODE

<span style="color:yellow"> Cria um script para iniciar o arquivo ``index.js`` </span>

- O nome do atalho será start
- Você cria na pasta ``package.json/scripts``
```json
"start":"node dist/index.js
```

![[Pasted image 20230916104840.png|500]]


- Para rodar no terminal:
```shell
npm run start
//ou
npm start
```
 >[!note]
 >como e um comando previsto pelo node, pode usar o comando somente ``start`` que o node inicia.
 >você pode colocar qualquer nome

- - -
<span style="color:orange">Criando um script(atalho) para watch mode</span>(monotorar em tempo real)
![[Pasted image 20240106093342.png]]
- O comando `tsc -w` é uma abreviação para "TypeScript Compiler Watch Mode" (Modo de Observação do Compilador TypeScript). Quando você executa esse comando, o TypeScript vai compilar seus arquivos `.ts` em tempo real, observando mudanças nos arquivos e recompilando-os automaticamente conforme as alterações são feitas. Isso é útil durante o desenvolvimento para garantir que seu código TypeScript seja compilado continuamente enquanto você trabalha.
- O nome do atalho será watch-ts

```json
"watch-ts":"tsc -w"
```
- Para iniciar no terminal:

``` shell
npm run watch-ts
```

---
# Processo para rodar node
1. watchmode
```shell
npm run watch-ts
```
2. Rodar o projeto
```shell
npm run start
//ou
npm start
```