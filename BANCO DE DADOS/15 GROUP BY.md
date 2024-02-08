- Agrupar
# Pega a lista de produtos e agrupa por fornecedor
```sql
SELECT * FROM produtos GROUP BY id_fornecedor;
```
![[Pasted image 20240207220412.png|500]]

-  Geralmente usa-se combinado com o count, avg ou o sum 
### Quantos unidades de produtos tem na loja:

```sql
SELECT SUM(estoque) AS estoqueTotal FROM produtos GROUP BY id_fornecedor;
```
![[Pasted image 20240207220755.png]]
