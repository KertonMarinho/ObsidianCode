- Junta informações de duas tabelas
- Subquery é um comando dentro de outro comando
- USA COM CUIDADO, ELE INTERAGE COM TODAS OS VALORES PARA FAZER A PESQUISA

### Junto dos nomes do produtos da tabela produtos colocar o nome do fornecedor da tabela fornecedores:
```sql
SELECT *, (SELECT forncedores.nome FROM fornecedores where fornecedores.id = produtos.id_fornecedor) as nome_fornecedores
```
- Select * = seleciona todos os campos da tabela produtos (from produtos)
- vírgula= campo virtual
- Dentro do parênteses o reesultado chamara de nome_fornecedor(as nome_fornecedor)
-  (SELECT forncedores.nome FROM fornecedores where fornecedores.id = produtos.id_fornecedor)
	- Selecione o nome de fornecedor onde (where) id for igual há produtos.id_fornecedor 

![[Pasted image 20240208192615.png|500]]

### Pega o produto de forncedor sem saber o id, usando só o nome do fornecedor(usando uam query em where):
```sql
SELECT * FROM produtos
WHERE (SELECT fornecedor.nome from fornecedor WHERE fornecedor.id = produtos.id_fornecedor) = 'NASA';
```
![[Pasted image 20240208194612.png|400]]
