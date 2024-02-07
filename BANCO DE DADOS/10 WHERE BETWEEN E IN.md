# BETWEEN
- Significa entre
- Ele substitui este código:
```sql
SELECT * FROM produtos WHERE estoque >= 5 and = 10;
```
- por este:
```sql
SELECT * FROM produtos WHERE estoque BETWEEN 5 AND 10;
```
![[Pasted image 20240206221527.png|400]]

---
# IN
- PESQUISA POR UMA LISTA ESPECIFICA
- Ele substitui este código:
```sql
SELECT * FROM produtos WHERE id_fornecedor = 1 OR Id_fornecedor
```
- Por este:
```sql
SELECT * FROM produtos WHERE id_fornecedor IN (1,6);
//Pega todos os itens do fonecedor que tiver  dentro da lista específica
```