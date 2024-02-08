- São funções de agregação
## <span style="color: #00FF00">Count</span> 
- Ele conta quantos itens têm e cada condição:
##### Conta em todas as condições
```sql
SELECT COUNT(*) FROM produtos
```
![[Pasted image 20240207214514.png|200]]
#### Quantos produtos tem no campo id_fornecedor igual a 6:
```sql
SELECT COUNT(*) FROM produtos WHERE id_fornecedor = 6;
```
![[Pasted image 20240207214800.png]]

## Colocar um nome real(renomear) ao atributo count(recurso chamado alias, uma coisa que quer dizer outra)
```sql
SELECT COUNT(*) AS contagem FROM produtos WHERE id_fornecedor = 6;
```
![[Pasted image 20240207215034.png]]

----
# <span style="color: #1E90FF">Avg</span>
- Média
### Média dos preços do campo preco:
```sql
SELECT AVG(preco) AS media FROM produtos;
```
![[Pasted image 20240207215413.png]]

## Média e a contagem:
```sql
SELECT AVG(preco) AS media, COUNT(*) AS contagem+ FROM produtos;
```
![[Pasted image 20240207215625.png]]

---
# <span style="color:#20B2AA">Sum</span>
- soma
### Soma do estoque
```sql
SELECT SUM(estoque) AS soma FROM produtos;
```
![[Pasted image 20240207220016.png]]