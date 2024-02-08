-  Dar maior flexibilidade na busca dos itens
- Pega itens que contém determinada string no inicio, meio ou fim

## <span style="color:yellow">EXEMPLO</span>
- pegar usuario que começa com Bonieky:
```sql
SELECT * FROM usuarios WHERE nome LIKE 'BONIEKY';
```
- Pega usuário que começa com Bonieky e tudo que vem depois dele:
```sql
SELECT * FROM usuarios WHERE nome LIKE 'BONIEKY%';
```
![[Pasted image 20240206220403.png|400]]
- Pega usuário que começa com Bonieky e tudo que vem antes dele( inverso ):
```sql
SELECT * FROM usuarios WHERE nome LIKE '%Lacerda';
```
![[Pasted image 20240206220541.png|400]]
- Pega string que esta no meio da frase ou algum lugar:
```sql
SELECT * FROM usuarios WHERE nome LIKE '%Lacerda%';
```

