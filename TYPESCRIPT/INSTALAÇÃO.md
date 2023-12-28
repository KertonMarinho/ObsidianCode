1.  Instale o Nodejs antes.
2. Instale o Typescript
```shell
c:\users\kerton> npm install -g typescript
```
- Para checar se estar instalado:
```shell
c:users\kerton> tsc --version
//version 4.3.2
```
3. Criar um novo arquivo chamado ``script.ts
4. Exemplo de código typescript:
	- Declarando que o valor de uma variável é vai ser um elemento HTML(ou seja ele vai ter value).
![[Pasted image 20231219223934.png]]
5. Agora entre na pasta do projeto pelo terminal
6. Converta o typescript Usando o terminal
```typescript
c:\projetos\typescript tsc <nome do arquivo que  comveter>
```

7. cria uma pasta ``public`` e outra pasta ``src``(significa código fonte), o HTML e o javascript vai para pasta pública e o typescript vai para pasta src
8. de o comando no terminal para que quando se converte o typescript para js ele cria o arquivo js na pasta desejada(src)
```bash
c:/projetos\typescript src/script.ts --outDir public
//outDir= auto pult diretory
```

9. coloca as tipagens no valor n1 e n2
```typescript
function calcular(n1: number, n2: number){
	return n1 + n2;
}
```

>[!warning]
>O value de todo elemento HTML sempre retornará por padrão uma string

- Então o valor(do value) deve ser convertido para número(usando o sinal de mais ou o parseInt):
```typescript
botao.addEventListener('click', function(){
	res.innerHTTML = calcular(+numero1.value, +numero2.value);
})
```

10. Transforme o resultado de retorno em string com toString:

```typescript
botao.addEventListener('click', function(){
	res.innerHTTML = calcular(+numero1.value, +numero2.value).toString;
})
```