## Pelo site oficial
1. Abaixa no site oficial MySQL Community

![[Pasted image 20240126230032.png|300]]
2. Escolhe o sistan linux e a versão
![[Pasted image 20240126230209.png|300]]
3. Procure por `deb package MySQL server`

![[Pasted image 20240126230320.png|400]]

---
## Pelo terminal
1. Primeiro atualiza o update
```shell
sudo apt-get update
```
2. Instale o servidor
```shell
sudo apt-get install mysql-server
```
3. Configurar a istalação
```shell
sudo mysql_secure_installation
```
- de um `ok`
- Digite o nível de senha(0  para mais simples)
- Digite a senha escolhida, duas vezes
- Digite ok
- remover usuário anônimo: yes
- desabilitar o login remoto: no
- remover o banco de dados de teste: no
- Recarregar os privilégios no que foi configurado agora; yes

4. Entre no root do MySql
```shel
sudo mysql
```
5. Verificação para ver o tipo e o processo de senha que está o usuário root, para que consiga conectar em dispositivos externos de forma fácil sem que precise usar sockets
```shell
SELECT user, plugin, host FROM mysql.user;
```

![[Pasted image 20240126231927.png]]- 
- Trocar `auth_socket`para `caching_sha2_password`recomendado pelo mysql
```shell
ALTER USER 'root'@'localhost' IDENTIFIED WITH caching_sha2_password BY '1234';
//1234 e a senha que vc escolheu do Mysql
```
- Como a senha `1234`e fraca vai dar o alerta de não corresonde a politica de acesso do mysql
- Para ver o que se pede na senha, digite o comando:
```shell
SHOW VAIRABLES LIKE 'validate_password%';
```
![[Pasted image 20240126232550.png]]
- Você pode desabilitar algumas exigências:
- Desabilite o check-user que impede de usar o nome root
```shell
SET GLOBAL validate_password.check_user_name = OFF;
```
- Modifique o número de caracteres da senha;
```shell
SET GLOBAL validate_password.length = 4;
```
- Desabilite caractere especial;
```shell
SET GLOBAL validate_password.special_char_count = 0;
```
- Agora de comando de novo para modificar o socket para  caching
```shell
ALTER USER 'root'@'localhost'IDENTIFIED WITH caching_sha2_password BY '1234';
```
6. Atualiza todos os privilégios 
```shell
FLUSH PRIVILEGES;
```
- De ocomando de volta para confirma mudanças
```shell
SELECT user, plugin, host FROM mysql.user;
```
7. Tenta agora entrar no mysql sem sudo:
```shell
mysql -u root -p
```
- Digite a senha e aparecerá as informações do mysql
![[Pasted image 20240126233929.png|450]]
- veja se o servidor esta funcionando com o comando:
```shell
systemctl status mysql.service
```
![[Pasted image 20240126234227.png|450]]

- se não tiver  funcionado digite este comandp;
```shell
systemctl start mysql
```
>[!info]
>
Thiago de Oliveira Cordeiro
No meu caso, foi necessário rodar também a última linha.   
>`SET GLOBAL validate_password.check_user_name = OFF;  SET GLOBAL validate_password.length = 4;  SET GLOBAL validate_password.special_char_count = 0;   SET GLOBAL validate_password.policy = LOW;  `

