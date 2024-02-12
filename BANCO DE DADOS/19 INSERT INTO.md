- inserir dados no banco de dados
```sql
INSERT INTO usuarios(nome, cadastro) VALUES ('Fulano', '2020-12-30');
```

- cadastrar mais de um cadastro
```sql
INSERT INTO usuarios(nome, cadastro) VALUES ('Fulano', '2020-12-30'), ('Beltrano', '2019-01-02');
```

- Usar a data do dia usando uma função do próprio SQL
```SQL
INSERT INTO usuarios(nome, cadastro) VALUES ('ZEFINHA', NOW());
```