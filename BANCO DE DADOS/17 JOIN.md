- ele é susbtituto do subquery
- Comando que usa na query que possibilita juntar duas ou mais tabelas e trocar informações sobre essas tabela
# Join #1
- ``SELECT  FROM produtos inner join fornecedores`` => junta a tabela produtos com a tabela fornecedores
![[Pasted image 20240208195649.png]]

#### Juntar as tabelas e escolhe quela campos
```sql
SELECT 
produtos.id, produtos.preco, produtos.estoque, fornecedor.nome AS fornecedor
FROM produtos INNER JOIN fornecedores on fornecedores.id = produtos,id_fornecedores;
```
![[Pasted image 20240208200450.png|400]]
