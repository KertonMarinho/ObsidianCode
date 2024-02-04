# TABELA USUÁRIO
1. Cria a tabela para acrescentar novos usuários
![[Pasted image 20240129222224.png|500]]
2. Coloca o nome de `usuários`
3. Adicione os campos:
	- ID
	- nome
	- data de cadastro
![[Pasted image 20240129222445.png|400]]
4. Na coluna ID colque já index primario
![[Pasted image 20240129222555.png|400]]
5. Na coluna ID coloque `auto_increment`
![[Pasted image 20240129222709.png|300]]
6. O nome coloque o tipo `varchar` com o tamanho `100` e <u>não permitir nulo</u>
7. A data de cadastro coloque o tipo `date` e <u>não permitir nulo</u> 
---
# TABELA PRODUTOS
1. Cria nova tabela chamado produtos
2. Adicionar as colunas:
	- id
	- nome
	- preco
	- estoque
	- minestoque
3. A coluna do Id será `primario`  e `auto_increment`
4. O nome será do tipo `varchar` com tamanho`150` e <u>não permitir nulo</u>
5. O preço será do tipo `float`  e <u>não permitir nulo</u>
6. O estoque será será do tipo `int`, <u>não permitir nulo</u> e coloque um valor padrão `0`:
![[Pasted image 20240129223757.png|200]].
7. O minestoque será do tipo `int`,  <u>não permitir nulo</u> e coloque um valor padrão `0`

---
# TABELA DOS FORNCEDORES
1. Cria nova tablea para os fornecedores
2. Adicione as colunas:
	- ID
	- Nome
	- Telefone
3. A coluna do ID terá `chave primaria` e `auto-increment
4. O nome será `varchar` e tamanho em `100`e <u>não permitir nulo</u>
5. Telefone será `Varchar`(pois o telefone possui caracteres), 
---
# RELAÇÃO ENTRE TABELAS(PRODUTO X FORNCEDORES
- Usa-se o campo ID por exemplo fornecedores para refêrenciar outras tabelas
1. Na tabela `Produto` cria uma coluna com oo nome `id_fornecedor`, tipo int  e não permitir nulo
- Com o arquivo do professor cadastre os produtos, usuários e fornecedores
 2. Do usuário
![[Pasted image 20240204114203.png]]
3. Do Produto: 
![[Pasted image 20240204114239.png]]
4. fornecedores:
![[Pasted image 20240204114311.png]]


> [!SUMMARY] Inserção de dados™
> Pra quem não entendeu, é só no HeidiSQL, "consulta", copia os dados que ele informou:
 > INSERT IGNORE INTO `usuarios` (`id`, `nome`, `datacadastro`) VALUES  
(1, 'Bonieky', '2007-12-10'),  
(2, 'Pedro', '2009-04-15'),  
(3, 'João', '2011-03-18'),  
(4, 'Jéssica', '2019-07-22'),  
(5, 'Beatriz', '2021-01-11');             
>
>aperte o em executar, ou F9, depois só da F5 pra atualizar, os dados serão importados.

