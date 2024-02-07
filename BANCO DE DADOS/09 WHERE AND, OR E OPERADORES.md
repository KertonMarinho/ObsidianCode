#  COMPARAÇÃO COM DOIS CAMPOS
```SQL
SELECT * FROM produtos WHERE estoque > minestoque
```
![[Pasted image 20240206214314.png|500]]

---
#  Colocar duas condições
 ```sql
 SELECT * FROM produtos WHERE preco = 200 AND preco = 140;
 
```
# com or
```sql
 SELECT * FROM produtos WHERE preco = 200 or preco = 140; 
```
![[Pasted image 20240206214734.png|500]]

# com duas AND
```sql
 SELECT * FROM produtos WHERE preco > 140 AND preco < 1000 AND id_fornecedor = 3;
 
```

# Quando for usar na mesma query o OR e o AND, coloque entre parêntese a conta que queira ser feito primeiro, o resultado pode mudar depedendo com vc faz a conta:
```sql
 SELECT * FROM produtos (WHERE preco > 140 AND preco < 1000) or id_fornecedor = 6;
 
```
- ou a condição AND ou a condição or for satisfeita