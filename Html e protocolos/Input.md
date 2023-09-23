<span style="color:pink">Atalho para cabeçalho</span> 

```
HTML 5
```
---
<span style="color:yellow">Formulario,metodo de enviar</span>
![[Pasted image 20230922214950.png]]
```html
<form method="get" action="teste.jsp"></form>
Method - forma que for Enviar
Method Get = geralmente formulário de busca
Method post - geralmente formulário de cadastro
Method action = para onde será enviado
``` 
---
<span style="color:yellow">Input text</span>
![[Input.png]]
```html
<input type="text" name="nome"></input>
input - entrada de dados-
type - tipo de entrada
atributo name - como vai chamar internamente este campo
```


---
<span style="color:yellow">Input radio</span>
![[Pasted image 20230922214639.png]]

```html
<input type="radio" name="tamanho" value="g">grande
```
---
<span style="color:yellow">Metodo para deixar um pradrão marcado na seleção(CHECKED)</span>
![[Pasted image 20230922215407.png]]

```html
<input type="radio" name="tamanho" value="g" checked >grande
```
---
<span style="color:yellow">Input select</span>
- caixa de seleção

```html
sabor<select name="sabor">
	<option>calabresa</option>
	<option>napolitana</option>
	<option>marguerita</option>
```
![[Pasted image 20230922215912.png]]

---
<span style="color:yellow">Input checkbox</span>
![[Pasted image 20230922220307.png]]
```html
<input type ="checkbox" name="borda" value="sim">borda
<input type ="checkbox" name="queijo" value="sim">queijo extra
```

---
<span style="color:yellow">Input email</span>
![[Pasted image 20230922220503.png]]

```html
Email:<input type="email" name="email">
```
---
<span style="color:yellow">Input date</span>
![[Pasted image 20230922220807.png|200]]

```html
Email:<input type="date" name="data de entrega">
```
---
<span style="color:yellow">texte area</span>
- Campo de texto maior
![[Pasted image 20230922221158.png|200]]
```html
<textarea name="mensagem" rows="10" cols="30"></textarea>
rows - linhas e
cols - colunas
```
---
<span style="color:yellow">input submit</span>
- submeter se em envio
![[Pasted image 20230922221705.png]]

```html
<input type="submit">
```
<span style="color:red">obs:</span> 
- Tudo que se inscreve no formulário aparece no link de acesso
![[Pasted image 20230922221940.png]]
- isso para o método Get
- para o método Post não aparece no link
![[Pasted image 20230922222200.png]]
---
