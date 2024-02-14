- ALTERA DADOS DO BANCO DE DADOS:
``comando de atualizar(udpadte) -> nome da tabela que quer atualizar (usuarios) -> o quer modificar junto, valor midificado(nome= 'Pedro da silva') -> em que quer mododificar(where) -> condição para achar os registros que vai mudar(id = 2;)``

```sql
UPDATE usuario SET nome = 'Pedro da Silva' WHERE id = 2;
```
- Para mais de um registro:
```sql
UPDATE usuario SET nome = 'Pedro da Silva',data_cadastro = '2024-02-13' WHERE id = 2;
```
<span style="color:orange">Exemplo</span>
```sql
UPDATE produtos SET preco = preco * 1,1 WHERE id_fornecedor = 6;
```

# Update sem where
- Perigoso
```sql
	UPDATE usuario SET nome = 'Kerton';
```
- Ele vai em todos os registro de usaurio e mudar o nome para kerton
## DICA:
- para não correr o risco de ter update sem where vc já escreva antes set where já colocando a condição  e depois  colocar o novo valor
1. set where antes
```sql
UPDATE usuario SET WHERE id = 2;
```
2. Depois colocar o valor:
```sql
UPDATE usuario SET nome = 'Kerton' WHERE id = 2;
```