= Ordena os produtos descrente ou crescente
```sql
SELECT * FROM produtos ORDER BY estoque ASC; // OU DESC
...by (qual campo ordenar)(acendente ou decedente)
```
- Se houver uma condição deve ser posto antes da ordenação:
```sql
SELECT * FROM produtos WHERE id_fornecedor =6  ORDER BY estoque ASC;
```
![[Pasted image 20240207211754.png]]

### Ordene por um campo e neste campo ordene por ordem alfabética:
```sql
SELECT * FROM produtos ORDER BY mineestoque ASC, nome ASC;
```
![[Pasted image 20240207212113.png|400]]

