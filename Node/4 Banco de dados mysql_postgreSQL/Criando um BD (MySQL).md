1. De dois cliques no banco de dados para conrctar
![[Pasted image 20240428220238.png]]
2. Visualizar a lista de tabelas
banco de dados(127.0.0.1) > teste > properties > tables
![[Pasted image 20240428220436.png|500]]
3. Cria uma nova tabela
botão direito > nova tabela
![[Pasted image 20240428220535.png|500]]

4. Cria uma lista de usuários com o nome users
5. Cria uma coluna em users com o nome de id
![[Pasted image 20240428220715.png|500]]
6. Configure a coluna id:
	1. int
	2. [v] para ``not full``
	3. [v] para auto inclement

7. Agora selecione ela com chave primária
	1. selecione id
	2. Botão direito
	3. new constraint from selection
		![[Pasted image 20240428221102.png|300]]
		![[Pasted image 20240428221139.png|300]]
8. cria outra coluna chamada nome e configure para:
		1. varchar(100)
		2. not null [v]
		3. auto inclement [v]
		4. Coloque um valor padrão (default =18),se o usuário não especificar a idade será 18 anos
9. Agora salve as interações
- em save
 ![[Pasted image 20240428221617.png|300]]
 - Aparece o comando que vai ser executado, confira e confirme
![[Pasted image 20240428221756.png|300]]
10. Agora coloca os dados nas tabelas criadas
![[Pasted image 20240428221934.png|500]]
- Para adicionar clique no +
![[Pasted image 20240428222043.png|500]]
- Acrescenta o nome ``bonieky``  e idade ``90``
![[Pasted image 20240428222144.png]]
- Acrescenta o nome`paulo` e idade `30`
- Acrescenta o nome `Joana` e idade `15`
- Acrescenta o nome `chico`  e idade `55`
- clique em `save`
