
* <span style="color:yellow">Whoami</span> - retorna o nome do usuário
* <span style="color:yellow">sudo su</span> -transforma-o em root (para sempre)
* <span style="color:yellow">exit</span> - sair do usuário, sai também do super usuário
* <span style="color:yellow">clear(ou CTRL+L)</span> limpa a tela do terminal 
****
* no Ubunto todos arquivos que forem azul são diretórios e em branco arquivos comuns

![[Pasted image 20230913213857.png]]

****
 Linha do terminal:
```shel
nomeDoUsuário@nomeDaMáquina:~$
```
<mark style="background: #ADCCFFA6;">Exemplo:</mark>
<span style="color:green">vinicios@vinicios-Inspiron -13-5378:~$</span>
* O til significa que estamos na pasta Home
* Sequilha(#) significa que está no root
	* <span style="color:green">root@vinicios-Inspiron -13-5378:/home/vinicios# </span>
****
<span style="color:orange">Comando touch</span>
* Muda a data e a hora que um arquivo foi criado
* Também pode ser usado para criar arquivos vazios(caso o touch seja usado com arquivo que não existam, por padrão ele criará estes arquivos)
* Sintaxe:

```shel
touch [opções] [arquivo]
ex: $ touch aula.txt
```
* <span style="color:red">-c</span> (não cria arquivos que não existam; por padrão o suao do touch sem argumentos fax que arquivo inexistente sejam criados com tamanho zero -arquivos vazios)
****
<span style="color:orange">Comando nano</span>
* Editor de texto
* Sintaxe:
```bash
nano arquivo
```
* abre o gnu nano(editor de texto Ubuntu)
****
<span style="color:orange">Comando cat</span>
* Lista um conteúdo de um arquivo
* Também serve para concatenar arquivos(juntar arquivos)
* Sintaxe:
```bash
cat arquivo
```
