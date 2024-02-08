- Limitar determinado resultado
### Quatro primeiros itens da lista de produtos
```sql
SELECT * FROM produtos LIMIT 4;
```

### Quatro primeiros mais caros da lista
```sql
SELECT * FROM produtos ORDER BY preco LIMIT 4;
```
### Pula um item e mostre 3:
- começa em zero;

```sql
SELECT * FROM produtos LIMIT 1,3;
```

![[Pasted image 20240207213426.png]]

### Pula seis item e mostra três:
- começa em zero;
```sql
SELECT * FROM produtos LIMIT 6,3;
```
![[Pasted image 20240207213610.png|400]]

### Pega o primeiro Pedro mais velho:

```sql
SELECT * FROM usuario WHERE nome = 'Pedro' ORDER BY datacadastro LIMIT 6,3;
```
![[Pasted image 20240207214047.png]]
