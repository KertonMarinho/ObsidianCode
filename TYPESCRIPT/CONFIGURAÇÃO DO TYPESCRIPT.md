# USANDO O WATCHMODE NO ARQUIVO
- Compila automaticamente o arquivo JS para o TP 
```shell
C:\\PROJETOS\TYPESCRIPT src/script.ts -w  //ou -wathmode
```

- Inicia a compilação em Watchmode(modo de escuta)
![[Pasted image 20231228153643.png]]
- Para sair do Watchmode use ``crtl+c``
---
---
# CRIANDO O ARQUIVO ``tsconfig.json``
1. Crie o arquivo``tsconfig``
```shell
tsc --init
```
![[Pasted image 20231228155056.png|300]]
- Pode combinar o TSC com Watchmode
```shell
tcs -w
//ou
tcs -watchmode
```
---
---
# ESCOLHENDO  QUAIS ARQUIVOS COMPILAR
- Configurar arquivos que não ser compilados pelo TP
1. Cria arquivo ``exculde`` na pasta ``tsconfig.json``
```json
//logo apos os arquivos padrão do json,log apos a virgula e antes da chave que fecha
"exclude":[
"src/outro.ts" //exemplo
]
```
![[Pasted image 20231229094132.png|300]]
- Geralmente se exclui arquivos de desenvovimento
- Pode-se excluir todos arquivos de determinada extensão usando ``*``:
```json
},
"excluide":[
	"*.dev.ts"
]
``` 
- Para excluir arquivo``.dev`` de qualquer pasta que achar, usa-se ``**/`` :
```json
},
"excluide":[
	"**/*.dev.ts"
]
``` 
- Como excluir uma pasta:
```json
},
"excluide":[
	"node_modules"
]
``` 
---
## incluindo arquivo para ser compilado
- Apartir do uso``include`` o TP se limitar a compilar só que estar nesta página

```json
"include": [
	"src/script.ts"
]
```
---
# Entendendo o Target
- Vc coloca a versão do JS que vc quer seja o alvo final do arquivo
- Por padrão ele vem com Ecmascript 5
![[Pasted image 20231229104115.png|200]]
---
# TRABALHANDO COM LIBS NO TYPESCRIPT
- Adicionado bibliotecas
- ver aula ``B7WEN/typescript/modulo 3:configuração do Typescript/#5:Trabalhando com libs no Typescript``
- Descomente no arquivo Json e acrescente a biblioteca
![[Pasted image 20231229111323.png|300]]
----
# ROOTDIR E OUTDIR
## <span style="color:orange">outDir</span>
- Define o diretório onde p compilador deve colocar os arquivos JS gerados a partir arquivos TP.
![[Pasted image 20231229112107.png]]
## <span style="color:aquamarine">rootDir</span> 
- Define o diretório onde o compilador deve procurar os arquivos Typescript de  origem
- Mesma coisa que o lib
- Geralmente usa-se junto com  o outDir
 ![[Pasted image 20231229112426.png]]
 ---

# noComment, noEmit e no Emit e noEmitOnError

## <span style="color:salmon">removeComments</span> 
- Remover os comentários do código
![[Pasted image 20231229112809.png|260]]

## <span style="color: #1E90FF">noEmit</span>
- Não gera arquivos compilados
- Geralmente para ver os erros do código
- Pouca utilidade plática
![[Pasted image 20231229113126.png|260]]


## <span style="color: #00FF00">noEmitOnError</span> 
- Este não vem como padrão,vc tem que acrescentar no jasone colocar true
- Ele compila e cria arquivos com erros
![[Pasted image 20231229113313.png|260]]
---
# CONFIGURAÇÃO PARA QUALIDADE DO CÓDIGO
## <span style="color:#20B2AA">noUnusedLocals</span>
- Ele avisa que quando cria uma variável e ela não está sendo usado em nível local
![[Pasted image 20231229114121.png]]


![[Pasted image 20231229113910.png|400]]

## <span style="color:violet">noUnusedParameters</span> 
- avisa quando não está sendo utilizados parâmetros
![[Pasted image 20231229114207.png]]

![[Pasted image 20231229114403.png|500]]
## <span style="color:red">noImplicitReturns</span> 
- sem retorno explicitos
- Serve para reportar um erro quando nem todos os caminhos de código em uma função retornam um valor
- Por exemplo, se você definir o tipo  de retorno  de uma função como ``bolean `` ,mas não retornar anda em algum caso, o compilador irá reclamar
- Essa opção é útil para evitar que você esqueça de retornar um valor de tipo diferente do declarado. Isso pode causar bugs difíceis de detectar no código Js gerado.
 ![[Pasted image 20231229114606.png|260]]
 